---
layout: about
title: about
permalink: /
subtitle: Scientific Computing and Imaging Institute, University of Utah

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false

social: true
---

I am a PhD researcher in Computer Science working on developing mathematical and algorithmic methods to understand and translate structure in complex, high-dimensional data into interpretable and actionable insights.

My work focuses on uncovering meaningful organization in data where standard approaches often fail to provide insight. A primary area of focus is understanding structure in learned representations in machine learning models—for example, I have studied graph neural network models for molecular data and shown that their embeddings capture chemically meaningful structure such as scaffolds and functional groups using topological methods, and developed interactive visualization tools to enable domain experts to explore and interpret these representations.

My research draws on tools from topology, geometry, and algorithms to develop principled approaches for analyzing complex systems and uncovering structure that is not directly observable through conventional techniques. I apply these ideas across diverse domains, including cheminformatics, neuroinformatics and dynamic simulation data.

I am interested in applying and extending these methods to challenging real-world problems, particularly in biological and biomedical domains where understanding the structure of data and models is critical for decision-making.

## Projects

<div style="max-height: 900px; overflow-y: auto; padding-right: 12px;">
  {% assign sorted_projects = site.projects | sort: "importance" | reverse %}
  {% for project in sorted_projects %}
    <div class="card mt-3 p-3">
      <h3 class="card-title">{{ project.title }}</h3>

      {% if project.img %}
        <img
          src="{{ project.img | prepend: '/assets/img/' | relative_url }}"
          alt="{{ project.title }}"
          style="max-width: 100%; height: auto; margin-bottom: 1rem;"
        >
      {% endif %}

      {% if project.description %}
        <p>{{ project.description }}</p>
      {% endif %}

      <div class="card-text">
        {{ project.content }}
      </div>
    </div>
  {% endfor %}
</div>