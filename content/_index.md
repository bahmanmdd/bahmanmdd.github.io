---
title: Bahman Madadi
date: 2022-10-24
type: landing
description: 'Bahman Madadi - Assistant Professor at Université Gustave Eiffel & ENTPE, EMob-Lab (Energy & Mobility Laboratory). Research in Graph Neural Networks, Deep Learning, Transport Network Design, and Zero-Emission Mobility. Expert in GNN, optimization, and intelligent transportation systems.'

design:
  spacing: '0'

sections:
  - block: resume-biography-3
    content:
      username: admin
      text: ''
      # Archived: Download Resume button removed
      # button:
      #   text: Download Resume
      #   url: uploads/BahmanMadadi_Resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
        skills: ''
        languages: ''
    design:
      background:
        video:
          filename: background.mp4
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
      show_read_time: false
  - block: collection
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: true
    design:
      view: citation
  - block: collection
    id: talks
    content:
      title: Recent Talks
      count: 6
      filters:
        folders:
          - events
    design:
      view: article-grid
      columns: 2
      show_read_time: false
---
