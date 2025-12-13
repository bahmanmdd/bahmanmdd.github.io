---
title: Publications
date: 2022-10-24
type: landing

sections:
  # Featured/Highlighted Publications
  - block: collection
    content:
      title: Featured Publications
      subtitle: Highlights of my research contributions
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  
  # All Publications organized by date
  - block: collection
    content:
      title: Complete Publication List
      text: |
        **Publication Types:**  
        📄 Journal Articles | 🎓 Conference Papers | 📚 Book Chapters | 🎯 PhD Thesis | 📑 Technical Reports | 📝 Preprints | 📰 Popular Science
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
      columns: 1
---
