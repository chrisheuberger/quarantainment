---
layout: default
---

<div class="outer-wrapper">
  
  <main class="wrapper">

    <h1><span>Online Events</span><span>and Entertainment</span><span>for Quarantine</span></h1>

    <div class="eyebrow">
      <p>Filter by Event Type</p>
    </div>
    <div class="button-group-container">
      <div class="button-group filters-button-group">
        <button class="button is-checked" data-filter="*">show all</button>
        <button class="button btn-filter-live" data-filter=".filter-live">live</button>
        <button class="button btn-filter-recorded" data-filter=".filter-recorded">recorded</button>
        <button class="button btn-filter-museums" data-filter=".filter-museums">museums</button>
        <button class="button btn-filter-vr-ar" data-filter=".filter-vr-ar">AR + VR</button>
        <button class="button btn-filter-kids" data-filter=".filter-kids">kids</button>
        <button class="button btn-filter-lists" data-filter=".filter-lists">lists</button>
      </div>
    </div>

    <div class="grid-container">
      <div class="grid">

        <div class="grid-sizer"></div>

        {% assign a_start = "<a class='event-link' href='" %}
        {% assign a_middle = "' target='_blank' rel='noopener'>" %}
        {% assign a_end = "</a>" %}

        {% for event in site.data.data.events %}
          {% if event.live %}
            <div class="element-item filter-live grid-item"><p>{{ event.live | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.live-long %}
            <div class="element-item filter-live grid-item grid-item--height2"><p>{{ event.live-long | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.recorded %}
            <div class="element-item filter-recorded grid-item"><p>{{ event.recorded | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.recorded-long %}
            <div class="element-item filter-recorded grid-item grid-item--height2"><p>{{ event.recorded-long | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.museums %}
            <div class="element-item filter-museums grid-item"><p>{{ event.museums | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.museums-long %}
            <div class="element-item filter-museums grid-item grid-item--height2"><p>{{ event.museums-long | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.vr-ar %}
            <div class="element-item filter-vr-ar grid-item"><p>{{ event.vr-ar | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.vr-ar-long %}
            <div class="element-item filter-vr-ar grid-item grid-item--height2"><p>{{ event.vr-ar-long | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.kids %}
            <div class="element-item filter-kids grid-item"><p>{{ event.kids | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.kids-long %}
            <div class="element-item filter-kids grid-item grid-item--height2"><p>{{ event.kids-long | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.lists %}
            <div class="element-item filter-lists grid-item"><p>{{ event.lists | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% elsif event.lists-long %}
            <div class="element-item filter-lists grid-item grid-item--height2"><p>{{ event.lists | replace: "[[", a_start | replace: "[+]", a_middle | replace: "]]", a_end }}</p></div>
          {% endif %}
        {% endfor %}

      </div>
    </div>

  </main>

  <footer>
    <p>Created by <a href="https://radishlab.com/" target="_blank">Radish Lab</a> | Suggestions welcome! Submit them <a href="mailto:chris@radishlab.com" target="_blank">here</a>. | Donate to Feeding America <a href="https://www.feedingamerica.org/" target="_blank">here</a>.</p>
  </footer>
  
</div>
