---
layout: page
---

Hello! You have reached A test webpage of Nuero Bioinfornatics Core; this website is....

We are interested in Bioinformatocs, developing algorithms, and working on interesting projects in academia\industry. We do [research](https://neurobioinfo.github.io/papers/), and develop piplines\software [software](https://neurobioinfo.github.io/software/).

If you are interested in collaborating and doing some great work, please reach out to me via:

<div class="contact-buttons" style="line-height:160%;margin-left:30px;margin-top:10px">
<p>
<link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css">
<link rel="stylesheet" href="//neurobioinfo.github.io/css/academicons.css">
  <a href="mailto:neurobioinfo@mcgill.ca" target="_blank" style="color:#855f65;"><i class="fa fa-envelope" style="font-size:1em"></i> &nbsp; Email<br></a>
<a href="https://github.com/neurobioinfo" target="_blank" style="color:#0e5295;"><i class="fa fa-github" aria-hidden="true"></i> &nbsp; GitHub<br></a>
</p>
</div>

<ul>
---
    Bioinfo 's Adv
---
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
  {% endfor %}
    
</ul>

<br>


 



