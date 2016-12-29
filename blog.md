---
layout: default
title: Blog
---


<header id="blog"  role="banner">
	<div class="container">
		<div class="row">
			<h1>{{page.title}}</h1>
		</div>
	</div>	
</header> 

<div class="container">
  <div class="panel panel-default">
    <div class="panel-body">
		{% for post in site.posts %}
			<div class="row">
				 <div class="col-sm-4 col-md-4 col-lg-4">
					 <h5 style="text-align: right">
					 	{{ post.date | date: "%b %-d, %Y"  }}
					 </h5>
				 </div>
				 <div class="col-sm-8 col-md-8 col-lg-8">
					 <h5 style="text-align: left">
					 	<strong><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></strong>
					 </h5>
				 </div>
			</div>
	    {% endfor %}
	</div>
  </div>
</div>