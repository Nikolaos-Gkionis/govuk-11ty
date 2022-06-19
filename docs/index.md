---
homepage: true
layout: product
includeInBreadcrumbs: true
description: Documentation using Markdown and published using GOV.UK styles.
image:
  src: /assets/NCTS-EU-UK-Map.png
  alt: NCTS EU UK map with HMRC logo.
startButton:
  href: "https://docs.google.com/presentation/d/1Mha2CB5-lYUafHUuX-QACJVDdPhV7c-_vZWob1Ufd7g/edit#slide=id.g113ede980a4_0_583"
  text: Alpha deck
eleventyComputed:
  title: "{{ pkg.description }}"
  ogImage:
    alt: "{{ options.homeKey }}"
---

<div class="govuk-grid-row">
{% for item in collections["homepage"] %}
  <section class="govuk-grid-column-one-third-from-desktop govuk-!-margin-bottom-8">
    <h2 class="govuk-heading-m govuk-!-font-size-27">{{ item.data.title }}</h2>
    <p class="govuk-body">{{ item.data.description | markdown("inline") }}</p>
    <p class="govuk-body"><a class="govuk-link govuk-!-font-weight-bold" href="{{ item.url | url }}">Link to the {{ item.data.title | lower }}</a></p>
  </section>
{% endfor %}
  <section class="govuk-grid-column-full">
    <hr class="govuk-section-break govuk-section-break--visible govuk-section-break--xl govuk-!-margin-top-0">
    <h2 class="govuk-heading-m govuk-!-font-size-27">Prototype</h2>
    <p class="govuk-body">The prototype for this service is currently in version-8</p>
    <p class="govuk-body">Username: prototype</p>
    <p class="govuk-body">Password: thisisabadpassword</p>
    <p class="govuk-body"><a class="govuk-link govuk-!-font-weight-bold" href="{{ pkg.repository.url | replace(".git", "") }}">View this prototype</a></p>
  </section>
</div>
