<div class="jumbotron">
    {% include carousel.html height="65" unit="%" duration="4" number="1" %}
    <!-- <img src="/img/group.jpg" class="d-block w-100" alt="..."> -->
    <h1 class="display-4">Navigation, Aerial-robots, and Perception Planning Lab (NappLab)</h1>
    <p class="lead">The <strong>Navigation, Aerial-robots, and Perception Planning Lab (NappLab)</strong>  is a research group in <a href="https://www.mines.edu/">Colorado School of Mines</a> CS Department. We study aerial robotics, active perception, and multi-robot systems with applications to aerial videography, infrastructure inspection, and physical search (mine safety, search and rescue). </p>
    <p> We are always looking out for talented students to join us as full-time students / visitors. To know more, click on the link below.</p>
    <a class="btn mines-theme-blaster-blue text-white btn-lg" href="{{ site.base }}/contact.html" role="button">Learn more</a>
  </div>

<!--
<section>
    <div class="card shadow mb-4">
        <div class="card-header py-3 d-flex flex-row align-items-center justify-content-between">
            <h6 class="m-0 font-weight-bold text-primary text-lg">News</h6>
        </div>
        <div class="card-body">
            {% for post in site.posts limit: site.front_page_news %}
            {% include news-item.html item=post %}
            {% endfor %}
            {% assign numposts = site.posts | size %}
            {% if numposts >= 1 %}
                <a href="{{ site.base }}/blog.html" class="btn btn-primary btn-icon-split btn-sm">
                    <span class="icon text-white-50">
                    <i class="fa fa-history"></i>
                    </span>
                    <span class="text">More news &hellip;</span>
                </a>
            {% endif %}
        </div>
    </div>
</section>
-->

<section>
    <div class="card shadow mb-4">
        <div class="card-header py-3 d-flex flex-row align-items-center justify-content-between">
            <h6 class="m-0 font-weight-bold text-primary text-lg">Projects</h6>
        </div>
        <div class="card-body">
            {% comment %}
            Sort the projects by date, putting those without dates last
            {% endcomment %}
            {% assign projects_by_date = site.projects | sort: 'last-updated', 'first' %}
            {% assign projects_by_date = projects_by_date | reverse %}
            {% for p in projects_by_date %}
              {% include project-card.html project=p %}
            {% endfor %}
            <p>
                <a href="{{ site.base }}/research.html" class="btn mines-theme-blaster-blue text-white btn-icon-split btn-sm">
                  <span class="icon text-white-50">
                  <i class="fa fa-robot"></i>
                  </span>
                  <span class="text">All projects&hellip;</span>
                </a> 
            </p>
        </div>

    </div>  
</section>

