---
layout: default
title: Blog
image: /assets/images/blogBanner.jpg
imageTxt: Our blog
---

<div class="pageBanner">
  <img width="1000" height="200" src="{{page.image}}" alt="{{page.imageTxt}}"/>
</div>
<div class="mainContent">
<h1>Latest Posts</h1>

{% for post in site.posts %}
<section class="post section" itemprop="blogPost" itemscope="itemscope" itemtype="http://schema.org/BlogPosting">
    <div class="section-inner">
        <div class="content">
            <div class="item">
                <div class="list-image">
                    <a href="{{ post.url }}"><img  itemprop="image" src="/assets/images/blog/{{ post.id | remove_first:'/' | replace_first:'/','-' | replace_first:'/','-' | replace_first:'/','_' | replace:'/','-' }}_small.jpg" alt="{{ post.title }}"/></a>
                </div>
                <div class="info text-left">
                    <h2 class="title" itemprop="headline"><a href="{{ post.url }}">{{ post.title }}</a></h2>

                    <p class="meta">
                        <span class="date" itemprop="datePublished">{{ post.date | date:'%m/%d/%Y'}}</span> - by
                        <span itemprop="author">{{ post.author }}</span>
                    </p>
                </div>
                <div class="desc text-left" itemprop="articleBody">                                    
                    {{ post.excerpt }}
                </div><!--//desc-->
                <div style="position:relative;">
                       <span class="more"><a class="btn btn-cta-secondary" href="{{ post.url }}">Read more</a></span>
                <div style="clear:both;"></div>
                </div>
            </div><!--//item-->                       
        </div><!--//content-->  
    </div><!--//section-inner-->                 
</section><!--//section-->

{% endfor %}
    
</div>
