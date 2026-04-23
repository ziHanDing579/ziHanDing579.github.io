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
* M.S. in Computer Science, University of Pittsburgh, 2026(Expected)
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
    * A Python environment package for both Windows and Linux environments
    * Updated old Conan package to newer Conan standards
  * Updated Poetry packages
  
Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
