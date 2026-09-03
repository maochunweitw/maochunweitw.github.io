---
layout: default
title: 索引
permalink: /index/
---

<section class="index-page">

  <div class="section-heading">
    <h2>索引</h2>
    <span>CONTENTS</span>
  </div>

  <p class="index-note">
    淳文字不提供傳統搜尋框，文章主要透過九大分類與索引閱讀。以下提供標籤與年份封存兩種方式，協助你找到想看的文字。
  </p>

  <section class="index-section">

    <div class="section-heading">
      <h2>標籤</h2>
      <span>TAGS</span>
    </div>

    <ul class="tag-list" id="tag-list">

      {% for tag in site.tags %}

        <li
          class="tag-item"
          data-tag="{{ tag[0] | escape }}"
        >

          <a
            href="{{ '/index/' | relative_url }}?tag={{ tag[0] | uri_escape }}"
          >

            <span class="tag-name">
              {{ tag[0] }}
            </span>

            <span class="tag-count">
              {{ tag[1].size }} 篇
            </span>

          </a>

        </li>

      {% endfor %}

    </ul>

    <p
      class="index-note"
      id="tag-limit-note"
      style="display:none;"
    >
      目前顯示最常用的 50 個標籤。
    </p>

  </section>


  <section
    class="index-section"
    id="archive"
  >

    <div class="section-heading">
      <h2>封存</h2>
      <span>ARCHIVE</span>
    </div>


    {% assign archive_years =
      site.posts |
      group_by_exp: "post", "post.date | date: '%Y'"
    %}


    {% for year in archive_years %}

      <div
        class="archive-year-group"
        data-year="{{ year.name }}"
      >

        <h3 class="archive-year-heading">

          <a
            href="{{ '/index/' | relative_url }}?year={{ year.name }}"
          >
            {{ year.name }}
          </a>

        </h3>


        <div class="archive-posts">

          {% for post in year.items %}

            <article
              class="post-card archive-item"
              data-year="{{ year.name }}"
              data-tags="{{ post.tags | join: '||' | escape }}"
            >

              <div class="post-meta">
                {{ post.date | date: "%Y.%m.%d" }}
              </div>


              <h3>

                <a href="{{ post.url | relative_url }}">
                  {{ post.title }}
                </a>

              </h3>

            </article>

          {% endfor %}

        </div>

      </div>

    {% endfor %}


    <div
      class="index-filter"
      id="index-filter"
      style="display:none;"
    >

      <a href="{{ '/index/' | relative_url }}">
        ← 顯示全部文章
      </a>

    </div>

  </section>

</section>


<style>

.index-page {
  width: 100%;
}


.index-section {
  margin-top: 55px;
}


.index-section:first-of-type {
  margin-top: 35px;
}


.index-note {
  max-width: 760px;
  margin: 20px 0 0;
  color: var(--muted);
  font: 13px/1.8 var(--sans);
}


.tag-list {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  column-gap: 50px;

  margin: 0;
  padding: 0;

  list-style: none;
  border-top: 1px solid var(--line);
}


.tag-item {
  border-bottom: 1px solid var(--line);
}


.tag-item a {
  display: flex;
  align-items: baseline;
  justify-content: space-between;

  gap: 18px;

  padding: 14px 0;

  color: var(--ink);
  text-decoration: none;
}


.tag-item a:hover,
.archive-year-heading a:hover,
.index-filter a:hover {
  color: var(--accent);
}


.tag-name {
  font-size: 17px;
}


.tag-count {
  flex-shrink: 0;

  color: var(--muted);

  font: 12px/1.5 var(--sans);
}


.archive-year-group {
  margin-top: 48px;
}


.archive-year-heading {
  margin: 0;

  padding-bottom: 14px;

  border-bottom: 1px solid var(--line);

  font-size: 27px;
  font-weight: 500;
}


.archive-year-heading a {
  color: var(--ink);
  text-decoration: none;
}


.archive-item {
  padding: 22px 0;
}


.archive-item h3 {
  margin-bottom: 0;
}


.index-filter {
  margin-top: 55px;

  padding-top: 20px;

  border-top: 1px solid var(--line);

  font: 13px/1.5 var(--sans);
}


.index-filter a {
  color: var(--accent);
}


@media (max-width: 700px) {

  .index-section {
    margin-top: 45px;
  }


  .tag-list {
    grid-template-columns: 1fr;
  }


  .tag-item a {
    padding: 13px 0;
  }


  .tag-name {
    font-size: 17px;
  }


  .archive-year-group {
    margin-top: 40px;
  }


  .archive-year-heading {
    font-size: 24px;
  }


  .archive-item {
    padding: 20px 0;
  }

}

</style>


<script>

document.addEventListener("DOMContentLoaded", function () {


  const tagList =
    document.getElementById("tag-list");


  const tagItems =
    tagList
      ? Array.from(
          tagList.querySelectorAll(".tag-item")
        )
      : [];


  const tagLimit = 50;


  const totalTags =
    tagItems.length;


  const tagLimitNote =
    document.getElementById("tag-limit-note");


  /*
   * 中文依筆畫排序。
   * 若瀏覽器不支援 stroke collation，
   * 則退回一般中文排序。
   */

  if (tagList && tagItems.length) {

    let collator;

    try {

      collator =
        new Intl.Collator(
          "zh-Hant-u-co-stroke",
          {
            numeric: true,
            sensitivity: "base"
          }
        );

    } catch (error) {

      collator =
        new Intl.Collator(
          "zh-Hant",
          {
            numeric: true,
            sensitivity: "base"
          }
        );

    }


    tagItems.sort(function (a, b) {

      return collator.compare(
        a.dataset.tag || "",
        b.dataset.tag || ""
      );

    });


    tagItems.forEach(function (item, index) {

      item.style.display =
        index < tagLimit
          ? ""
          : "none";

      tagList.appendChild(item);

    });


    if (
      totalTags > tagLimit &&
      tagLimitNote
    ) {

      tagLimitNote.style.display =
        "block";

    }

  }


  const params =
    new URLSearchParams(
      window.location.search
    );


  const selectedTag =
    params.get("tag");


  const selectedYear =
    params.get("year");


  const groups =
    Array.from(
      document.querySelectorAll(
        ".archive-year-group"
      )
    );


  const posts =
    Array.from(
      document.querySelectorAll(
        ".archive-item"
      )
    );


  const indexPage =
    document.querySelector(
      ".index-page"
    );


  const archive =
    document.getElementById(
      "archive"
    );


  const filter =
    document.getElementById(
      "index-filter"
    );


  const filterTitle =
    document.createElement("p");


  filterTitle.className =
    "index-note";


  function applyFilter() {

    if (
      !selectedTag &&
      !selectedYear
    ) {

      return;

    }


    if (selectedTag) {

      filterTitle.textContent =
        "目前顯示標籤：「" +
        selectedTag +
        "」";


      indexPage.insertBefore(
        filterTitle,
        archive
      );


      posts.forEach(function (post) {

        const tags =
          (post.dataset.tags || "")
            .split("||")
            .filter(Boolean);


        post.style.display =
          tags.includes(selectedTag)
            ? ""
            : "none";

      });

    }


    if (selectedYear) {

      filterTitle.textContent =
        "目前顯示：" +
        selectedYear +
        " 年";


      indexPage.insertBefore(
        filterTitle,
        archive
      );


      posts.forEach(function (post) {

        post.style.display =
          post.dataset.year === selectedYear
            ? ""
            : "none";

      });

    }


    groups.forEach(function (group) {

      const visiblePosts =
        Array.from(
          group.querySelectorAll(
            ".archive-item"
          )
        ).some(function (post) {

          return (
            post.style.display !==
            "none"
          );

        });


      group.style.display =
        visiblePosts
          ? ""
          : "none";

    });


    if (filter) {

      filter.style.display =
        "block";

    }

  }


  applyFilter();

});

</script>
