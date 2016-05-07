---
layout: soc
title: SoC
permalink: /soc/
banner: /images/soc.jpg
---

<!-- Banner -->
<section id="banner" style="background-image:url({{ page.banner }})">
    <div class="inner">
        <h2>Seasons Of Code</h2>
        <p> an initiative by <a href="https://stab-iitb.org/wncc">The Web and Coding Club, IIT Bombay</a></p>
        <ul class="actions">
            <li><a href="#one" class="button big special">Join The Force</a></li>
        </ul>
        <ul class="actions">
            <li><a href="#two" class="button big special">Projects</a></li>
        </ul>
    </div>
</section>

<!-- Three -->
<section id="three" class="wrapper style1">
	<div class="container">
		<div class="row">
			<div class="8u">
				<section>
					<h2>What is Seasons of Code?</h2>
					<a href="#" class="image fit"><img src="/images/coding.jpg" alt="" /></a>
					<p>Seasons of Code is a programme launched by the WnCC, along the lines of GSoC without much greenery though. The incentive is similar to ITSP, based on the current form of it, the fundamental difference is that one can choose from the ideas offered by mentors who are senior undergrads, doctorate students or professors, and in some exceptional cases, startups. We plan to have a really long timeframe though, until the next winter extending this programme into a mentorship of sorts into the semester. It is not just about development by the way. We have some mentors ready to take up programmes regarding competitive coding and scientific computation too.
</p>
				</section>
			</div>
			<div class="4u">
				<section>
					<h3>Why should you participate?</h3>
					<p>Seasons of Code gives you an amazing opportunity to learn and dive into coding under the mentorship of the best in our institute. Our list of projects gives you a chance to pick up and work on any topic you are enthusiastic about.</p>
					<ul class="actions">
						<li><a href="#two" class="button alt">Projects</a></li>
					</ul>
				</section>
				<hr />
				<section>
					<h3>Types of Projects</h3>
					<ul>
						<li>Open Source</li>
						<li>Competitive Coding</li>
						<li>Scientific Computation</li>
						<li>Development</li>					
					</ul>
				</section>
			</div>
		</div>
	</div>
</section>	

<section id="one" class="wrapper style2">
				<header class="major">
					<h2>Join The Force</h2>
					<p>Do. Or do not. There is no try.</p>
				</header>
				<div class="container">
					<div class="row">
						<div class="6u">
							<section class="special box">
								<img class="icon major" src="/svg/light-siber-one.svg">
								<h3>Padawan</h3>
								<p>The Force is strong with you. Train yourself to let go of everything you fear to lose. The Force will be with you always. Ready are you?</p><br>
<!-- TODO: Add Padawan form -->
								<a target = "_balnk" href="https://docs.google.com/forms/d/1uzp4XbKcTIiXMG9cvflzwnxpkAZVHpJ6jDJeQu7-45k/viewform" class="button big special">Become a Padawan</a>
							</section>
						</div>
						<div class="6u">
							<section class="special box">
								<img class="icon major" src="/svg/light-siber.svg">
								<h3>Master</h3>
								<p>I can feel you code. It gives you focus. It makes you stronger. Your focus determines your reality. Use the force and someday you will be the most powerful Jedi ever.</p>
								<a target = "_blank" href="https://docs.google.com/forms/d/1YHkyL1i2kdTJbAN2UJKcDa30u9Ed6wc0-pGfMl3FuKQ/viewform" class="button big special">Become a Master</a>
							</section>
						</div>
					</div>
				</div>
			</section>
			
<!-- Two -->
<section id="two" class="wrapper style1">
	<header class="major">
		<h2>List of Projects</h2>
		<p>Your eyes can deceive you. Don’t trust them.</p>
	</header>
	<div class="container">
		{% assign projects = site.soc_projects | sort:"weight"  %}
            {% for project in projects%}
            {% capture modulo %}{{ forloop.index0 | mod:3 }}{% endcapture %}
            {% if modulo == '0' or forloop.first %}
            	<div class="row">
            {% endif %}
				<div class="4u">
					<section class="special">
						<a href="{{ project.url }}" class="image fit"><img src="{{ project.image }}" alt="{{ project.title }}" /></a>
						<h3>{{ project.title }}</h3>
						<h4>- {{ project.mentor }}</h4>
						<p>{{ project.content | split:'<!--break-->' | first }}</p>
						<ul class="actions">
							<li><a href="{{ project.url }}" class="button alt">Learn More</a></li>
						</ul>
					</section>
				</div>
			{% if modulo == '2' or forloop.last %}
    			</div>
			{% endif %}
            {% endfor %}
		<div style="text-align: center;">
		<a href="#" class="button big special">View All Projects</a>
		</div>
	</div>
</section>			
