---
layout: page 
---


<style>
li p { 
    margin: 0
}
</style>


{% for c in site.data.articles %} 

### {{c.publisher.name}} {% if c.publisher.link %}<small>[↗]({{c.publisher.link}})</small>{%endif%}

{% for article in c.publisher.articles %} 
* {% if article.pre%}{{article.pre|safe}}{%endif%} [{{article.name}}]({{article.link}}) {% if article.post%}{{article.post|safe}}{% endif %}
{% endfor %}
{% endfor %}

### Technical Reviewer
{% for c in site.data.reviews %} 
 * [{{c.name}}]({{c.link}}), {{c.author}}{% if c.publisher %}, {{c.publisher }}{% endif %}
{% endfor %}

### Interviews
{% for c in site.data.interviews %} 
 * [{{c.name}}]({{c.link}}){% if c.publisher %}, {{c.publisher }}{% endif %}
{% endfor %}


More writing available on <a href="https://glasnt.com/blog">musings</a>. 
[Header image](https://unsplash.com/photos/vZJdYl5JVXY) via [unsplash.com](https://unsplash.com)
