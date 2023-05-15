{% for clip in site.clips %}
[{{ clip.title }}]({{ clip.url  | absolute_url }})


{% endfor %}
