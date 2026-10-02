---
layout: page
title: courses
permalink: /courses/
description: Course notes written to make hard subjects easier to follow, grouped by subject.
nav: true
nav_order: 6
nav_dropdown_data: courses
---

<!-- _pages/courses.md -->
<div class="courses">
  <nav class="course-subjects" aria-label="Subjects">
    {% for subject in site.data.courses %}
      <a href="#{{ subject.id }}"><i class="{{ subject.icon }}"></i> {{ subject.name }}</a>
    {% endfor %}
  </nav>

  {% for subject in site.data.courses %}
    <section class="course-subject" id="{{ subject.id }}">
      <h2 class="category">{{ subject.name }}</h2>
      {% if subject.blurb %}<p class="course-subject-blurb">{{ subject.blurb }}</p>{% endif %}

      {% if subject.courses.size > 0 %}
        {% for course in subject.courses %}
          <article class="course-card">
            <div class="course-card-head">
              <h3>{{ course.title }}</h3>
              <div class="course-meta">
                {% if course.level %}<span>{{ course.level }}</span>{% endif %}
                {% if course.sections %}<span>{{ course.sections }} sections</span>{% endif %}
              </div>
            </div>
            {% if course.description %}<p class="course-description">{{ course.description }}</p>{% endif %}
            {% if course.topics %}
              <ul class="course-topics">
                {% for topic in course.topics %}<li>{{ topic }}</li>{% endfor %}
              </ul>
            {% endif %}
            <div class="course-editions">
              {% for edition in course.editions %}
                <a class="course-edition" href="{{ edition.url | relative_url }}"{% if edition.download %} download{% endif %}>
                  <i class="{{ edition.icon }}"></i>
                  <span>
                    <strong>{{ edition.label }}</strong>
                    {% if edition.note %}<small>{{ edition.note }}</small>{% endif %}
                  </span>
                  <i class="fa-solid {% if edition.download %}fa-download{% else %}fa-arrow-right{% endif %} course-edition-arrow"></i>
                </a>
              {% endfor %}
            </div>
          </article>
        {% endfor %}
      {% else %}
        <p class="course-empty">Coming soon.</p>
      {% endif %}
    </section>
  {% endfor %}
</div>
