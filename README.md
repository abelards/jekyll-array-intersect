# jekyll-array-intersect
Array intersection for Jekyll: Ruby's `a &amp; b`

## Caution
This is an experiment. I'm probably doing things wrong.
This is also a Work In Progress. The goal is to have a self-filtering list.

I can't believe this wasn't in Liquid's standard commands since it's used for shops and related products.
So I'm probably doing something really wrong.


## How to use
These three lines will help you find common tags/topics/categories.
Use `intersection` to get a boolean, `intersect` to get an array

## With ArrayIntersect
`{{ assign related = a | intersection: b }}`

## Without ArrayIntersect
I was just trying to to a stupid "related posts" on my blog!
 ```
      {% assign related = false %}
      {% assign ts = post.topics | split:',' %}
      {% assign refs = page.topics | split:',' %}
      {% for t in ts %}{% for ref in refs %}
      {% if t == ref %}{% assign related = true %}{% endif %}
      {% endfor %}{% endfor %}
      {% if related and (post.title != page.title) %} WOOHOO  {% endif %}
 ```

