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
					<h2>Mollis ut adipiscing</h2>
					<a href="#" class="image fit"><img src="/images/pic03.jpg" alt="" /></a>
					<p>Vis accumsan feugiat adipiscing nisl amet adipiscing accumsan blandit accumsan sapien blandit ac amet faucibus aliquet placerat commodo. Interdum ante aliquet commodo accumsan vis phasellus adipiscing. Ornare a in lacinia. Vestibulum accumsan ac metus massa tempor. Accumsan in lacinia ornare massa amet. Ac interdum ac non praesent. Cubilia lacinia interdum massa faucibus blandit nullam. Accumsan phasellus nunc integer. Accumsan euismod nunc adipiscing lacinia erat ut sit. Arcu amet. Id massa aliquet arcu accumsan lorem amet accumsan commodo odio cubilia ac eu interdum placerat placerat arcu commodo lobortis adipiscing semper ornare pellentesque.</p>
				</section>
			</div>
			<div class="4u">
				<section>
					<h3>Magna massa blandit</h3>
					<p>Feugiat amet accumsan ante aliquet feugiat accumsan. Ante blandit accumsan eu amet tortor non lorem felis semper. Interdum adipiscing orci feugiat penatibus adipiscing col cubilia lorem ipsum dolor sit amet feugiat consequat.</p>
					<ul class="actions">
						<li><a href="#" class="button alt">Learn More</a></li>
					</ul>
				</section>
				<hr />
				<section>
					<h3>Ante sed commodo</h3>
					<ul class="alt">
						<li><a href="#">Erat blandit risus vis adipiscing</a></li>
						<li><a href="#">Tempus ultricies faucibus amet</a></li>
						<li><a href="#">Arcu commodo non adipiscing quis</a></li>
						<li><a href="#">Accumsan vis lacinia semper</a></li>
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
								<a target = "_blank" href="" class="button big special">Become a Padawan</a>
							</section>
						</div>
						<div class="6u">
							<section class="special box">
								<img class="icon major" src="/svg/ondem-jedi.svg">
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
		<div class="row">
		{% assign projects = site.categories.projects | sort:"weight"  %}
            {% for post in projects limit:5%}
			<div class="4u">
				<section class="special">
					<a href="#" class="image fit"><img src="{{ post.image }}" alt="" /></a>
					<h3>{{ post.title }}</h3>
					<h4>- {{ post.mentor }}</h4>
					<p>{{ post.description }}</p>
					<ul class="actions">
						<li><a href="#" class="button alt">Learn More</a></li>
					</ul>
				</section>
			</div>
            {% endfor %}
		</div>
		<div style="text-align: center;">
		<a href="#" class="button big special">View All Projects</a>
		</div>
	</div>
</section>			
