---
layout: page
permalink: /
title: About
nav: About

address: <a href="https://www.google.com/maps/place/University+of+Calgary/@51.0775908,-114.140695,15z/data=!4m5!3m4!1s0x0:0x36aff4a9e3c803fb!8m2!3d51.0775908!4d-114.140695" class="page-description" target="_blank">University of Calgary, Alberta, Canada</a>
---

<div class="col p-0 pt-4 pb-4">
  <h1 class="pb-3 title text-left font-weight-bold">Chris Nielsen</h1>
  {% if page.address %}
      <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.address }}</h6>
  {% endif %}
</div>


<!-- Introduction -->

<div style="display: flex; flex-wrap: wrap;">
    <div class="text-justify p-0">
        <div class="col-xs-12 col-sm-6 p-0 pt-2 pb-sm-2 pb-4 pl-sm-4 text-center" style="float: right;">
          <img class="profile-img img-responsive" src="{{ 'prof_pic.jpg' | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" width="100">
        </div>

        <p>
            I am currently pursuing a PhD in Biomedical Engineering, Medical Imaging specialization, at the University of Calgary under the supervision of Dr. Nils Forkert. 
        </p>
        
        <p>
            I graduated with an MSc in Electrical Engineering in 2019 and a BSc in Applied Mathematics in 2016, both from the University of Calgary. My MSc thesis focused on the challenge of training machine learning models for medical image classification where there is a limited volume of data. From 2017 until joining the MIPLAB in 2021, I worked as an industrial data scientist at Getty Images, applying machine learning to improve image search. My research interests involve developing machine learning tools for ophthalmology. I aspire to become a physician-scientist specializing in ophthalmology and balancing direct surgical intervention with research and policy at the intersection of artificial intelligence and medicine.
        </p>
    </div>
</div>

<div class="col text-justify p-0">
    <p>

    </p>

</div>



<!-- News -->
<div class="news mt-3 p-0">
  <h1 class="title mb-4 p-0">news</h1>
  {% assign news = site.news | reverse %}
  {% for item in news limit: site.news_limit %}
    <div class="row p-0">
      <div class="col-sm-2 p-0">
        <span class="badge light-green darken-1 font-weight-bold text-uppercase align-middle date ml-3">
          {{ item.date | date: "%b %-d, %Y" }}
        </span>
      </div>
      <div class="col-sm-10 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 font-weight-light text">
        <p>{{ item.content | remove: '<p>' | remove: '</p>' | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>
