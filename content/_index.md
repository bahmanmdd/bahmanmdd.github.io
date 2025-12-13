---
title: Bahman Madadi
date: 2022-10-24
type: landing
description: 'Bahman Madadi - Assistant Professor at Université Gustave Eiffel & ENTPE, EMob-Lab (Energy & Mobility Laboratory). Research in Graph Neural Networks, Deep Learning, Transport Network Design, and Zero-Emission Mobility. Expert in GNN, optimization, and intelligent transportation systems.'

design:
  spacing: '6rem'

sections:
  - block: resume-biography-3
    content:
      username: admin
      text: ''
      button:
        text: Download Resume
        url: uploads/BahmanMadadi_Resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
        skills: ''
        languages: ''
    design:
      css_class: hbx-bg-gradient
      avatar:
        size: medium
        shape: circle
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
  - block: collection
    id: talks
    content:
      title: Recent &amp; Upcoming Talks
      filters:
        folders:
          - events
    design:
      view: card
---
