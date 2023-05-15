{% for clip in site.clips %}
[{{ clip.title }}]({{ clip.url  | relative_url }})


{% endfor %}
