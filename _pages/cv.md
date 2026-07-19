---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* M.S. in Computer Science, University of Pittsburgh, 2026
* B.S. in Computer Science and Computational Biology, University of Pittsburgh, 2024

Work experience
======
* Summer 2025: DevOps Intern @ Ansys
  * Azure DevOps pipeline maintenance and updates
    * Removing redundant stages in main pipeline
    * Building a pipeline template for all Conan and Poetry packages
      * Building, testing, deployment
      * Generating SBOMs
  * Created and maintained Conan packages
    * A Python linked library package for both Windows and Linux environments
    * Updated old Conan package to newer Conan standards
  * Updated Poetry packages
  
* Fall 2024: Graduate Research Assistant @ University of Pittsburgh
  * Maintained OCCAM, a container orchestration platform for reproducing academic artifacts
    * Implemented feature to export entire workflow of containers to local directory
    * Created a hyperparameter optimization workflow for demonstration purposes
    * General debugging over a very large, legacy codebase
  
Skills
======
* Artificial Intelligence
  * Prompt Engineering
  * Model Fine-tuning
  * Model Training
* Machine Learning
  * PyTorch
  * Pandas
  * NumPy
  * Cuda
* Cybersecurity
  * Security Research
* Software Engineering
  * Flask
  * Springboot
  * SQL
  * ORM
* DevOps
  * Azure DevOps
  * GCP
  * Github Actions
  * Docker
  * Kubernetes

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Projects
=====
  <ul>{% for post in site.portfolio reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
