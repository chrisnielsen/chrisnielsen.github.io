---
layout: page
permalink: /blog/
title: blog
nav: blog
description: paper reviews, tutorials, ect.

---


## Contents
### [Paper Reviews](#paper-reviews)



<div id="projects" class="row mt-2 pt-3" style="overflow: visible !important;">
  {% assign sorted_projects = site.paper_reviews | sort: "importance" | reverse %}
  {% for project in paper_reviews %}
    <div class="project-card">
      {% if project.redirect %}
        <a href="{{ project.redirect }}" target="_blank">
      {% else %}
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
      {% endif %}
        <div class="card">
          <img class="card-img-top" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}" alt="project thumbnail">
          <div class="card-body">
            <h5 class="card-title text-lowercase">{{ project.title }}</h5>
            <p class="card-text">{{ project.description }}</p>
            <div class="row ml-1 mr-1 p-0">
              {% if project.wordpress %}
                <div class="wordpress-icon" data-toggle="tooltip" title="Blog Post">
                  <div class="icon">
                    <a href="{{ project.wordpress }}" target="_blank"><i class="fab fa-wordpress-simple wp-icon"></i></a>
                  </div>
                </div>
              {% endif %}
              {% if project.github %}
                {% assign github_id = project.title | append: project.github | replace: '/', '-' | replace: ' ', '-' %}
                <div class="github-icon">
                  <div class="icon" data-toggle="tooltip" title="Code Repository">
                    <a href="https://github.com/{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
                  </div>
                </div>
              {% endif %}
            </div>
          </div>
        </div>
      </a>
    </div>
  {% endfor %}
</div>





<a name="paper-reviews"></a>

<h3 class="mt-4">Paper Reviews</h3>


<div class="card mt-3">
  <div class="p-3">
    <div class="row">
      <div class="col-sm-10">
        <h5 class="font-weight-bold">Topics in Deep Learning</h5>
      </div>
      <div class="col-sm-2 text-left text-sm-right">
        <span class="badge font-weight-bold light-green darken-1 text-uppercase align-middle">
            10-707
        </span>
      </div>
    </div>
    <h6 class="font-italic mt-2 mt-sm-0">Fall 2017: Teaching Assistant</h6>
    <ul class="card-text font-weight-light list-group list-group-flush">
      <li class="list-group-item">○ Graduate level introduction to machine learning class for masters and PhD students taught by  <a href="https://www.cs.cmu.edu/~rsalakhu/" target="_blank">Prof. Ruslan Salakhutdinov</a>.</li>
      <li class="list-group-item">○ I mentored groups of students working on class projects, graded homeworks and exams.</li>
      <li class="list-group-item">○ Course materials can be found <a href="http://www.cs.cmu.edu/~rsalakhu/10707/" target="_blank">here</a>.</li>
    </ul>
  </div>
</div>




<h3 class="mt-4">Politehnica University of Timisoara</h3>
<div class="card mt-3">
  <div class="p-3">
    <div class="row">
      <div class="col-sm-10">
        <h5 class="font-weight-bold">Competitive Programming Seminar</h5>
      </div>
    </div>
    <h6 class="font-italic mt-2 mt-sm-0">Fall 2013, Spring 2014: Lecturer and course co-organizer</h6>
    <ul class="card-text font-weight-light list-group list-group-flush">
      <li class="list-group-item">○ I co-organized a <a href="https://www.meetup.com/Cerc-algoritmica-TM" target="_blank">competitive programming seminar</a> for university and high-school students interested to train for algorithmic competitions (e.g. ACM-ICPC, informatics olympiad).</li>
      <li class="list-group-item">○ I taught algorithms and data structures used in competitive programming, designed and solved practice problems and internal competitions.</li>
    </ul>
  </div>
</div>