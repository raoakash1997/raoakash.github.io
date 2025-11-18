---
layout: page
title: CS Research Seminar
permalink: /csgraduateseminar/
nav: true
nav_order: 3
description: Information and announcements for the CS Graduate Research Seminar at WSU.
---

# CS Graduate Research Seminar

The **CS Graduate Research Seminar** is a bi-weekly forum for graduate students to:

- Learn about current research in computer science  
- Practice asking good research questions  
- Build connections across labs, research areas, and career paths  

Pizza is usually provided 🍕, and everyone is encouraged to stay for informal discussion after the talk.

---

## Next / Latest Seminar

{% assign seminar_posts = site.seminars | sort: "date" | reverse %}

{% if seminar_posts.size > 0 %}
  {% assign latest = seminar_posts.first %}

  **Title:** [{{ latest.title }}]({{ latest.url | relative_url }})  
  **Date:** {{ latest.date | date: "%A, %B %-d, %Y" }}

  {{ latest.excerpt | strip_html | truncate: 260 }}

  [Read full announcement →]({{ latest.url | relative_url }})

{% else %}
  No seminar announcements yet. Check back soon!
{% endif %}


---

## About the Seminar

The **CS Graduate Research Seminar** is organized by and for graduate students in the  
School of Electrical Engineering and Computer Science (EECS) at Washington State University.

**Goals of the series:**

- Showcase ongoing research in CS and related areas  
- Help students practice presenting and critiquing research  
- Provide a low-pressure environment to ask questions  
- Connect students with potential collaborators and mentors  

**Typical logistics:**

- **When:** Bi-weekly, mid-day (usually 12:00–1:00 PM)  
- **Where:** VCEA EME 52 (unless otherwise noted)  
- **Who:** CS graduate students, faculty, and interested undergrads  

---

## Past Seminar Announcements

Below is a list of all seminar-related posts.


## Past Seminar Announcements

{% if seminar_posts.size > 1 %}
<ul class="post-list">
  {% for post in seminar_posts offset:1 %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h3>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <p>
        {{ post.excerpt | strip_html | truncate: 180 }}
      </p>
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No past seminars recorded yet.</p>
{% endif %}

---

## Get Involved

If you’re interested in:

- **Giving a talk**
- **Suggesting a speaker**
- **Helping with organization (posters, emails, logistics)**

please contact **Akash Rao** at **[akashgopinath.rao@wsu.edu]**.
