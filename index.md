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
* [{{article.name}}]({{article.link}})
{% endfor %}

{% endfor %}

### Technical Reviewer
{% for c in site.data.reviews %} 
 * [{{c.name}}]({{c.link}}), {{c.author}}{% if c.publisher %}, {{c.publisher }}{% endif %}
{% endfor %}

More writing available on <a href="https://glasnt.com/blog">musings</a>. 
[Header image](https://unsplash.com/photos/vZJdYl5JVXY) via [unsplash.com](https://unsplash.com)
