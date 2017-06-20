---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
---

<article>
  <header class="hero animated fadeInUp">
    <div class="mdc-layout-grid">
      <div class="mdc-layout-grid__cell mdc-layout-grid__cell--span-2 mdc-layout-grid__cell--span-0-phone">
      </div>
      <div class="mdc-layout-grid__cell mdc-layout-grid__cell--span-8 mdc-layout-grid__cell--span-4-phone">
        <h1 class="mdc-typography--display4">Your technology partner in business.</h1>
        <h2>We build custom, intuitive, scalable software.</h2>
        <h3><a href="{{ site.baseurl }}{% link about.md %}" aria-label="About">Learn more →</a></h3>
      </div>
    </div>
  </header>
  <section class="animated fadeInUp">
    <div class="mdc-layout-grid">
      <div class="mdc-layout-grid__cell mdc-layout-grid__cell--span-2 mdc-layout-grid__cell--span-0-phone">
      </div>
      <div class="mdc-layout-grid__cell mdc-layout-grid__cell--span-8 mdc-layout-grid__cell--span-4-phone">
        <h2 style="margin-top: 0;">Selected Projects</h2>
        <hr />
        {% for post in site.posts %}
          <div class="mdc-card" style="margin-bottom: 16px; padding: 16px; color: white; background-color: {{ post.color }};">
            <div class="mdc-layout-grid" style="--mdc-layout-grid-margin: 0;">
              <div class="mdc-layout-grid__cell mdc-layout-grid__cell--span-5 mdc-layout-grid__cell--span-4-phone">
                <img alt="{{ post.client }}" src="{{ site.url }}/assets/img/{{ post.logo }}" />
              </div>
              <div class="mdc-layout-grid__cell mdc-layout-grid__cell--span-7 mdc-layout-grid__cell--span-4-phone">
                <h3 style="margin-top: 0;">{{ post.client }}</h3>
                <p>{{ post.summary }}</p>
                <span><a href="{{ post.url }}">Read more →</a></span>
              </div>
            </div>
          </div>
        {% endfor %}
      </div>
      <div class="mdc-layout-grid__cell mdc-layout-grid__cell--span-2 mdc-layout-grid__cell--span-0-phone">
      </div>
    </div>
  </section>
</article>