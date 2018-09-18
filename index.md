---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# layout: home
---
This is a collection of notes mainly concerning software engineering. They are written as a reminder to myself about various topics, rather than a full in-depth how-to on any particular subject.

Hopefully you may also find something useful here.

{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% assign pages_list = category[1] %}  
    {% assign pages_list = pages_list | sort:"order" %}  
    {% for post in pages_list %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}