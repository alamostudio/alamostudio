---
layout: default
---

{% include hero.html %}
{% include google_review_app.html %}
{% include map_stats.html %}
{% for benefit in site.data.benefits %}
  {%- if benefit.position == "left" -%}
    {% include left_benefit.html
      headline=benefit.headline
      description=benefit.description
      image=benefit.image %}
  {%- else -%}
    {% include right_benefit.html 
      headline=benefit.headline
      description=benefit.description
      image=benefit.image
    %}
  {%- endif -%}
{%- endfor -%}
{% include about_us.html %}
{% include who.html %}
{% include cta.html %}
{% include calendly.html %}