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
            <a href="#{{ person.slug }}" class="speakers-link" data-toggle="modal">
                <div class="speakers-hover">
                    <div class="speakers-hover-content">
                        <i class="fa fa-plus fa-3x"></i>
                    </div>
                </div>
                <img src="{{ person.pic | relative_url }}" class="img-responsive img-centered" alt="">
            </a>
            <div class="speakers-caption">
                <h4 class="speakers-name">{{ person.name }}</h4>
                <p class="text-muted">{{ person.affiliation }}</p>
                <p class="text-muted">{{ person.role }}</p>
            </div>
        </div>
        {% endif %}
    {% endfor %}
</div>

{% for person in site.organizers %}
    {% if person.organizer_type == "chair" %}
        {% include people-modal.html person=person %}
    {% endif %}
{% endfor %}
## Technical program committee

<div class="row">
    {% for person in site.organizers %}
        {% if person.organizer_type == "tpc" %}
            {% include people-simple.html person=person %}
        {% endif %}
    {% endfor %}
</div>

## Web chair

<div class="row">
    {% for person in site.organizers %}
        {% if person.organizer_type == "web" %}
            {% include people-simple.html person=person %}
        {% endif %}
    {% endfor %}
</div>

## Publicity chair

<div class="row">
    {% for person in site.organizers %}
        {% if person.organizer_type == "publicity" %}
            {% include people-simple.html person=person %}
        {% endif %}
    {% endfor %}
</div>
