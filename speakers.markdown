---
layout: people
title: Invited Speakers
permalink: /speakers/
---

<div class="row">
    <div class="col-sm-12">
        <h2 class="section-heading">{{ page.title }}</h2>
    </div>
</div>
            
{% for person in site.speakers %}
{% if person.withPaper == false %}
<div class="row" id="speakers">
    <div class="col-sm-10 speakers-item">
        <div class="row">
            <div class="col-sm-2">
                <a href="#{{ person.slug }}" class="speakers-link" data-toggle="modal">
                    <div class="speakers-hover">
                        <div class="speakers-hover-content">
                            <i class="fa fa-plus fa-3x"></i>
                        </div>
                    </div>
                    <img src="{{ person.pic | relative_url }}" class="img-responsive img-centered" alt="">
                </a>
            </div>
            <div class="col-sm-10 speakers-info">
                <p><b>Name:</b> {{ person.name }} </p>
                <p><b>Affiliation:</b> {{ person.affiliation }} </p>
                <p><b>Topic:</b> {{ person.speach.topic }} </p>
            </div>
        </div>
    </div>
    <div class="col-sm-2"></div>
</div>
{% endif %}
{% endfor %}

<div class="row">
    <div class="col-sm-12">
        <h2 class="section-heading">Invited speakers with papers</h2>
    </div>
</div>

{% for person in site.speakers %}
{% if person.withPaper == true %}
<div class="row" id="speakers">
    <div class="col-sm-10 speakers-item">
        <div class="row">
            <div class="col-sm-2">
                <a href="#{{ person.slug }}" class="speakers-link" data-toggle="modal">
                    <div class="speakers-hover">
                        <div class="speakers-hover-content">
                            <i class="fa fa-plus fa-3x"></i>
                        </div>
                    </div>
                    <img src="{{ person.pic | relative_url }}" class="img-responsive img-centered" alt="">
                </a>
            </div>
            <div class="col-sm-10 speakers-info">
                <p><b>Name:</b> {{ person.name }} </p>
                <p><b>Affiliation:</b> {{ person.affiliation }} </p>
                <p><b>Topic:</b> {{ person.speach.topic }} </p>
            </div>
        </div>
    </div>
    <div class="col-sm-2"></div>
</div>
{% endif %}
{% endfor %}


{% for person in site.speakers %}
    {% include people-modal.html person=person %}
{% endfor %}
