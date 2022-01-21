---
layout: people
title: Organizers
permalink: /organizers/
---

## Chair

<div class="row" id="speakers">
    {% for person in site.organizers %}
        {% if person.organizer_type == "chair" %}
        <div class="col-sm-4 speakers-item">
            <a href="#{{ person.id }}" class="speakers-link" data-toggle="modal">
                <div class="speakers-hover">
                    <div class="speakers-hover-content">
                        <i class="fa fa-plus fa-3x"></i>
                    </div>
                </div>
                <img src="{{ person.pic | relative_url }}" class="img-responsive img-centered" alt="">
            </a>
            <div class="speakers-caption">
                <h4>{{ person.name }}</h4>
                <p class="text-muted">{{ person.affiliation }}</p>
                <p class="text-muted">{{ person.role }}</p>
            </div>
        </div>
        {% endif %}
    {% endfor %}
</div>