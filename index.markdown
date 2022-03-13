---
layout: home
title: Home
---

<div id ="intro-wrapper" class="l-middle">
	<div id="intro-title-wrapper" class="intro-left">
		<h1 id="intro-title">Hi, I'm Sheng-Yun (Anthony) Peng.</h1>
		<div id="intro-subtitle">
			I'm a CS PhD Student at Georgia Institue of Technology
		</div>
	</div>
	<div class="intro-left">
	<div class="intro-left">
		I am an active member of <img class="intro-logo" style="width: 19px; padding-bottom: 5px;" src="/images/poloclub.png"> <a href="http://poloclub.gatech.edu">Polo Club of Data Science</a>, where we conduct research spanning across computer vision, machine learning, human-centered AI and data visualization. My advisor is <a href="http://www.cc.gatech.edu/~dchau/">Prof. Polo Chau</a>
    </div>
	<div style="height: 1rem"></div>
	<div class="intro-left">
		My research focuses on adversarial machine learning. Currently, I am investigating how to defend the object detectors and object trackers against digital and physical attacks. 
	</div>
	<div style="height: 1rem"></div>
	<div>
		I have collaborated with researchers, developers, and scientists while working at 
        <img class="intro-logo" style="width: 19px; padding-bottom: 5px;" src="/images/gatech.svg"> Georgia Tech, 
        <img class="intro-logo" style="width: 18px; padding-bottom: 3px;" src="/images/intel.svg"> Intel Lab, 
        <img class="intro-logo" style="width: 24px" src="/images/ucla.svg"> UCLA Design Automation Lab, 
        <img class="intro-logo" style="width: 24px;" src="/images/tongji.svg"> Tongji International Joint Research Lab of Earthquake Engineering,
        <img class="intro-logo" style="width: 24px;" src="/images/aaii.png"> Shanghai Jiao Tong University Advanced Avionics and Intelligent Information Lab,
        and <img class="intro-logo" style="width: 24px;" src="/images/fudan.svg"> Fudan University.
	</div>
</div>

<div class="intro-right">
	<img id="intro-image" class="intro-right" src="/images/square.jpeg">
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
		<!-- <div id="intro-cv"><a href="/cv">Here's my CV.</a></div> -->
	</div>
	</div>
</div>

<hr class="l-middle home-hr">

<h2 class="feature-title l-middle">
	Featured <a href="/cv#publications">Research Publications</a>
</h2>
<div class="cover-wrapper l-screen">
	{% assign sortedPublications = site.categories.papers | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.featured == true and feature.feature-order <= 4%}
			    {% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>
<div class="cover-wrapper l-screen">
	{% assign sortedPublications = site.categories.papers | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.featured == true and feature.feature-order > 4%}
			    {% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>


<h2 class="feature-title l-middle">
	<a href="{{ site.url }}/everything-else" style="color: #303030">Everything Else</a>
</h2>
<div id="everything-else" class="l-middle">
	<a href="{{ site.url }}/projects"><div>Projects</div></a>
	<a href="{{ site.url }}/blog"><div>Blog</div></a>
    <a href="{{ site.url }}/useful-tools"><div>Useful Tools</div></a>
</div>


[gt]: http://www.gatech.edu "Georgia Tech"
[cse]: http://cse.gatech.edu "Georgia Tech Computational Science and Engineering"
[coc]: http://www.cc.gatech.edu "Georgia Tech College of Computing"

[cv]: {{ site.url }}/cv
[polo]: http://www.cc.gatech.edu/~dchau/ "Polo Chau"
[poloclub]: http://poloclub.gatech.edu "Polo Club of Data Science"
