---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

[Here is a link to my complete CV](/files/cv/cv.pdf).

Education
======
* Ph.D. in Mechanical Engineering, The University of British Columbia, 2023 (expected)
* M.Sc. in Aerospace Engineering, Sharif University of Technology, 2016
* B.Sc. in Aerospace Engineering, K. N. Toosi University of Technology, 2014

Work experience
======
* Sep 2019 - Present: Research Assistant
  * The University of British Columbia
  * Duties included:
	* Developed object-oriented software for stability analysis and improvement of different computational methods using C++ and Python.
	* Created a framework for eigenanalysis of the solution Jacobian and mesh optimization using PETSc and SLEPc, enabling current solvers to achieve stable and more reliable results.
  * Supervisor: [Prof. Carl Ollivier-Gooch](https://mech.ubc.ca/carl-ollivier-gooch/)
  
* Sep 2019 - Present: Teaching Assistant
  * The University of British Columbia
  * Duties included:
	* Conducted tutorials, designed and graded assignments, and provided laboratory guidance for courses including Aerodynamics of Aircraft, Fluid Dynamics, and Thermodynamics.
  
* Sep 2014 - Aug 2016: Research Assistant
  * Sharif University of Technology
  * Duties included:
	* Implemented reconfigurable hardware programming using C++ and Vivado Design Suite for hardware design and acceleration of computational problems.
  * Supervisor: [Dr. Abbas Ebrahimi](http://ae.sharif.edu/~portal/faculty/1286515506)
  
* Sep 2014 - Aug 2016: Teaching Assistant
  * Sharif University of Technology
  * Duties included:
	* Conducted tutorials, designed and graded assignments, and provided laboratory guidance for courses including  Computer Programming, Computational Fluid Dynamics, Computer Aided Design, and Seminar.
  
* Sep 2013 - Aug 2014: Research Assistant
  * K. N. Toosi University of Technology
  * Duties included:
	* Developed MATLAB software for computational speed-up of fluid flow and heat transfer simulations.
  * Supervisor: [Dr. Reza Ebrahimi](https://wp.kntu.ac.ir/rebrahimi/)

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
{% if false %}<!-- AHAMA removes the following section from the page -->
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
{% endif %}<!-- AHAMA removes the following section from the page -->
  
Service and leadership
======
* Undergraduate and graduate course teaching and mentoring

Languages
======
* English
* Kurdish
* Persian
