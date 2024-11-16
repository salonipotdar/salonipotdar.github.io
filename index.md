---
layout: home
title: Home
jsarr:
- js/scripts.js
---

<div id ="intro-wrapper" class="l-page">
	<div id="intro-title-wrapper" class="intro-left">
		<h1 id="intro-title">{{ site.title }}</h1>
		<div id="intro-subtitle">
			{{ site.tagline }} 
		</div>
	</div>
	<div class="intro-left">
	<div class="intro-left">
		I work on Natural Language Processing and machine learning research specifically in generative AI, question answering and conversational AI. I am a Senior AI/ML Manager in the Siri and Search team at Apple leading the query understanding and knowledge graph machine learning initiatives. I have 30+ patents and 20+ papers accepted at top conferences like ACL, EMNLP, NAACL, AAAI and KDD with over 1000+ citations.  
	</div>
	<div style="height: 1rem"></div>
	<div>
        Prior to this I was a Senior Staff Applied Scientist and Engineering Manager at IBM Watson where I designed and developed algorithms for IBM's conversational AI product - Watson Assistant. 
	</div>
	<div class="intro-left">
        I got my Masters degree at the Language Technologies Institute at Carnegie Mellon University in 2014. I was awarded the Women in AI Award - North America (Special Jury Recognition) in 2023 for my work in AI.  
	</div>
	<div style="height: 1rem"></div>
</div>

<div class="intro-right">
	<img id="intro-image" class="intro-right" src="/images/portrait.jpg">
	<div style="height: 0.5rem"></div>
	<div id="intro-image-links" class="intro-right">
		{% for link in site.data.social-links %}
			{% if link.on-homepage == true %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
	</div>
	<div style="height: 0.5rem"></div>
	<div id="intro-cv-wrapper" class="intro-right">
		{% for link in site.data.social-links %}
			{% if link.id == "cv-web" %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
	</div>
	</div>
</div>




<hr class="l-page">

# News
{% for news in site.data.news %}
{% include news.html news=news %}
{% endfor %}


<hr class="l-page">

# Publications and Patents

{% assign selectedBoolForBibtex = true %}
{% assign selected = site.data.publications %}
{% for pub in selected %}
{% include pubentry.html pub=pub %}
{% endfor %}


<!-- ### All Publications -->

{% assign selectedBoolForBibtex = false %}

<hr class="l-page">
