---
layout: page
permalink: /publications/
title: Publications
description:
nav: true
nav_order: 3
---

<div class="publication-browser" id="publication-browser">
  <div class="publication-toolbar">
    <div class="publication-search" role="search" aria-label="Search publications">
      {% include bib_search.liquid %}
    </div>
  </div>

  <div class="publication-tabs" role="tablist" aria-label="Publication categories">
    <button type="button" class="publication-tab is-active" role="tab" id="pub-tab-all" aria-controls="pub-panel-all" aria-selected="true" data-publication-tab="all">All</button>
    <button type="button" class="publication-tab" role="tab" id="pub-tab-journal" aria-controls="pub-panel-journal" aria-selected="false" data-publication-tab="journal" tabindex="-1">Journals</button>
    <button type="button" class="publication-tab" role="tab" id="pub-tab-conference" aria-controls="pub-panel-conference" aria-selected="false" data-publication-tab="conference" tabindex="-1">Conferences</button>
    <button type="button" class="publication-tab" role="tab" id="pub-tab-book" aria-controls="pub-panel-book" aria-selected="false" data-publication-tab="book" tabindex="-1">Books</button>
    <button type="button" class="publication-tab" role="tab" id="pub-tab-patent" aria-controls="pub-panel-patent" aria-selected="false" data-publication-tab="patent" tabindex="-1">Patents</button>
  </div>

  <div class="publication-panels">
    <section class="publication-panel" id="pub-panel-all" role="tabpanel" aria-labelledby="pub-tab-all" data-publication-panel="all">
      <div class="publications">
        {% bibliography %}
      </div>
    </section>
    <section class="publication-panel" id="pub-panel-journal" role="tabpanel" aria-labelledby="pub-tab-journal" data-publication-panel="journal" hidden>
      <div class="publications">
        {% bibliography --query @*[type=journal] --prefix journals- %}
      </div>
    </section>
    <section class="publication-panel" id="pub-panel-conference" role="tabpanel" aria-labelledby="pub-tab-conference" data-publication-panel="conference" hidden>
      <div class="publications">
        {% bibliography --query @*[type=conference] --prefix conferences- %}
      </div>
    </section>
    <section class="publication-panel" id="pub-panel-book" role="tabpanel" aria-labelledby="pub-tab-book" data-publication-panel="book" hidden>
      <div class="publications">
        {% bibliography --query @*[type=book] --prefix books- %}
      </div>
    </section>
    <section class="publication-panel" id="pub-panel-patent" role="tabpanel" aria-labelledby="pub-tab-patent" data-publication-panel="patent" hidden>
      <div class="publications">
        {% bibliography --query @*[type=patent] --prefix patents- %}
      </div>
      <p class="publication-empty" id="publication-patent-empty">No patents listed yet.</p>
    </section>
  </div>
</div>

<style>
/* Professional, responsive publication discovery controls. */
.publication-browser { --pub-accent: var(--global-theme-color, #2563eb); }
.publication-toolbar { display: flex; justify-content: flex-end; align-items: center; width: 100%; margin: 0 0 .85rem; }
.publication-search { width: min(100%, 170px); max-width: 170px; margin-left: auto; }
.publication-search > * { max-width: 100% !important; margin-left: auto !important; }
.publication-search input,
.publication-search #bibsearch,
.publication-search .bibsearch,
.publication-search input[type="search"],
.publication-search input[type="text"] {
  box-sizing: border-box !important; width: 100% !important; max-width: 100% !important;
  min-height: 38px; border-radius: 9px !important;
  padding: .47rem .8rem !important; font-size: .9rem !important;
}
.publication-tabs {
  display: flex; flex-wrap: wrap; align-items: center; gap: .35rem;
  padding: .35rem; margin-bottom: 1.3rem;
  border: 1px solid var(--global-divider-color, #dce1e7);
  border-radius: 12px; background: var(--global-card-bg-color, #fafafa);
}
.publication-tab {
  appearance: none; border: 1px solid transparent; background: transparent;
  color: var(--global-text-color, #263238); border-radius: 9px;
  font: inherit; font-size: .91rem; font-weight: 650;
  padding: .56rem 1.05rem; min-width: 110px; cursor: pointer;
  transition: background .15s ease, color .15s ease, box-shadow .15s ease;
}
.publication-tab:hover { background: rgba(100, 120, 180, .09); }
.publication-tab.is-active {
  background: var(--pub-accent); border-color: var(--pub-accent);
  color: #fff; box-shadow: 0 2px 8px rgba(0,0,0,.12);
}
.publication-tab:focus-visible { outline: 2px solid var(--pub-accent); outline-offset: 2px; }
.publication-panel[hidden] { display: none !important; }
.publication-panel .publications { margin-top: .3rem; }
.publication-panel .bibliography li { scroll-margin-top: 6rem; }
.publication-empty { border: 1px solid var(--global-divider-color, #dce1e7); border-radius: 12px; padding: 1.6rem; text-align: center; color: var(--global-text-color-light, #68717b); background: var(--global-card-bg-color, #fafafa); }

@media (max-width: 600px) {
  .publication-search { width: min(100%, 155px); }
  .publication-tabs { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: .3rem; }
  .publication-tab { min-width: 0; padding: .57rem .35rem; font-size: .85rem; }
}
@media (prefers-reduced-motion: reduce) { .publication-tab { transition: none; } }
/* Hide the duplicate page heading added by the theme. */
.post-header, .page-header { display: none !important; }
</style>

<script>
(function () {
  function initPublicationTabs() {
    const root = document.getElementById("publication-browser");
    if (!root) return;
    const tabs = Array.from(root.querySelectorAll("[data-publication-tab]"));
    const panels = Array.from(root.querySelectorAll("[data-publication-panel]"));
    const patentPanel = root.querySelector('[data-publication-panel="patent"]');
    const patentEmpty = document.getElementById("publication-patent-empty");
    if (patentPanel && patentEmpty) {
      patentEmpty.hidden = patentPanel.querySelectorAll(".bibliography li").length > 0;
    }
    function selectTab(selected, focus) {
      tabs.forEach(function (tab) {
        const active = tab === selected;
        tab.classList.toggle("is-active", active);
        tab.setAttribute("aria-selected", String(active));
        tab.tabIndex = active ? 0 : -1;
      });
      panels.forEach(function (panel) {
        panel.hidden = panel.dataset.publicationPanel !== selected.dataset.publicationTab;
      });
      if (focus) selected.focus();
      /* Reapply any existing bibliography search to the newly visible panel. */
      const input = root.querySelector('#bibsearch, input[id*="bibsearch"], input[id*="bib-search"]');
      if (input) input.dispatchEvent(new Event("keyup", { bubbles: true }));
    }
    tabs.forEach(function (tab, i) {
      tab.addEventListener("click", function () { selectTab(tab, false); });
      tab.addEventListener("keydown", function (event) {
        if (!["ArrowLeft", "ArrowRight", "Home", "End"].includes(event.key)) return;
        event.preventDefault();
        const next = event.key === "Home" ? 0 : event.key === "End" ? tabs.length - 1 :
          (i + (event.key === "ArrowRight" ? 1 : -1) + tabs.length) % tabs.length;
        selectTab(tabs[next], true);
      });
    });
  }
  if (document.readyState === "loading") document.addEventListener("DOMContentLoaded", initPublicationTabs);
  else initPublicationTabs();
})();
</script>
