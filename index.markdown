---
layout: home
title: Home
---

<div id ="intro-wrapper" class="l-middle">
	<div id="intro-title-wrapper" class="intro-left">
		<h1 id="intro-title">Hi, I'm ShengYun (Anthony) Peng.</h1>
		<div id="intro-subtitle">
			CS PhD Student at Georgia Institue of Technology
		</div>
	</div>
	<div class="intro-left">
	<div class="intro-left">
		I'm an active member of <img class="intro-logo" style="width: 19px; padding-bottom: 5px;" src="/images/poloclub.png"> <a href="http://poloclub.gatech.edu">Polo Club of Data Science</a> advised by <a href="http://www.cc.gatech.edu/~dchau/">Prof. Polo Chau</a>. 
    </div>
	<div style="height: 1rem"></div>
	<div class="intro-left">
		My research spans machine learning and computer vision. In particular, I have strong interests in building reliable algorithms and toolkits that understand, fortify and democratize AI security with an eye towards scalability and practicality in real-world settings. 
		<!-- focuses on adversarial machine learning. Currently, I am investigating how to defend the object detectors and object trackers against digital and physical attacks.  -->
	</div>
	<div style="height: 1rem"></div>
	<div>
		I have collaborated with researchers, developers, and scientists while working at 
        <img class="intro-logo" style="width: 19px; padding-bottom: 5px;" src="/images/gatech.svg"> Georgia Tech, 
        <img class="intro-logo" style="width: 18px; padding-bottom: 3px;" src="/images/intel.svg"> Intel Security Solutions Lab, 
        <img class="intro-logo" style="width: 24px" src="/images/ucla.svg"> UCLA Design Automation Lab, 
        <img class="intro-logo" style="width: 24px;" src="/images/tongji.svg"> Tongji University,
        <img class="intro-logo" style="width: 24px;" src="/images/aaii.png"> Shanghai Jiao Tong University,
        and <img class="intro-logo" style="width: 24px;" src="/images/fudan.svg"> Fudan University.
	</div>
</div>

<div class="intro-right">
	<img id="intro-image" class="intro-right" src="/images/2022-square.jpg">
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
		{% if feature.featured == true and feature.feature-order > 3 and feature.feature-order <= 6 %}
			    {% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>

<div style="height: 1rem"></div>
<div class="cover-wrapper l-screen">
	{% assign sortedPublications = site.categories.papers | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.featured == true and feature.feature-order <= 3 %}
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
