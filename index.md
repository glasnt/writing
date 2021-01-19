---
layout: page 
header-img: ../img/header_image.jpg
description: in which glasnt types the words
---

<style>
li p { 
    margin: 0
}
</style>

{% for c in site.data.articles %} 
{% if c.publisher.link %}
### [{{c.publisher.name}}]({{c.publisher.link}})
{% else %}
### {{c.publisher.name}}
{% endif %}
{% for article in c.publisher.articles %} 
* {% if article.pre%}{{article.pre|safe}}{%endif%} [{{article.name}}]({{article.link}}) {% if article.post%}{{article.post|safe}}{% endif %}
{% endfor %}
{% endfor %}

### Technical Reviewer
{% for c in site.data.reviews %} 
 * [{{c.name}}]({{c.link}}), {{c.author}}{% if c.publisher %}, {{c.publisher }}{% endif %}
{% endfor %}

More writing available on <a href="https://glasnt.com/blog">musings</a>. 
[Header image](https://unsplash.com/photos/vZJdYl5JVXY) via [unsplash.com](https://unsplash.com)
