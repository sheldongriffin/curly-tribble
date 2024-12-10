---
layout: my-fancy-layout
title: "Medical CV"
permalink: /medical-cv/
---

<h1>Medical CV: {{ site.data.medical_cv.name }}</h1>
<p><strong>Date of Birth:</strong> {{ site.data.medical_cv.date_of_birth }}</p>

<h2>Confirmed Diagnoses</h2>
<ul>
  {% for diagnosis in site.data.medical_cv.confirmed_diagnoses %}
    <li>
      <strong>{{ diagnosis.name }}</strong><br>
      <em>Diagnostic Evidence:</em> {{ diagnosis.diagnostic_evidence }}<br>
      <em>Treatment Plan:</em> {{ diagnosis.treatment_plan }}<br>
      <em>Treated and Compliant?</em> {{ diagnosis.treated_and_compliant | default: "Unknown" }}<br>
      <em>Related Symptoms:</em> {{ diagnosis.related_symptoms }}
    </li>
  {% endfor %}
</ul>
