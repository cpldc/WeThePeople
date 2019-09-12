---
---

<div>
        {% for post in site.posts %}
        {
    
          "title"    : "{{ post.title | escape }}",
          "url"      : "{{ site.baseurl }}{{ post.url }}",
          "category" : "{{ post.category }}",
          "tags"     : "{{ post.tags | join: ', ' }}",
          "authorfn" : "{{ post.author.first_name }}",
          "authorln" : "{{ post.author.last_name }}",
          "date"     : "{{ post.date }}"
    
        } {% unless forloop.last %},{% endunless %}
      {% endfor %}
</div>