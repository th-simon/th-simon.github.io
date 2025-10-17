---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '0rem'

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ''
      show_education: false
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/resume.pdf
      headings:
        about: 'About me'
        education: ''
        interests: ''
        experience: ''
    design:
      # Apply a gradient background
      css_class: hbx-bg-gradient
      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  - block: resume-experience
    id: education
    content:
      username: cv
    design:
      # Hugo date format
      date_format: 'January 2006'
      # Education or Experience section first?
      is_education_first: false
  - block: collection
    id: research
    content:
      title: Featured Research
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 3
  - block: collection
    content:
      title: Scholarly Publications
      text: ''
      filters:
        folders:
          - publications
        tags:
          - Adaptive Randomization
        exclude_featured: false
    design:
      view: citation
  - block: collection
    content:
      title: Working Papers
      text: ''
      filters:
        folders:
          - publications
        tags:
          - Job Market Paper
          - Working Paper
        exclude_featured: false
    design:
      view: citation
  - block: collection
    content:
      title: Work in Progress
      text: ''
      filters:
        folders:
          - publications
        tags:
          - Work In Progress
        exclude_featured: false
    design:
      view: citation
  - block: collection
    content:
      title: Professional Publications
      text: ''
      filters:
        folders:
          - publications
        tags:
          - Professional Publication
        exclude_featured: false
    design:
      view: citation
  - block: collection
    id: teaching
    content:
      title: Teaching
      filters:
        folders:
          - events
    design:
      view: card
  - block: collection
    id: ressources
    content:
      title: Ressources
      filters:
        folders:
          - ressources
    design:
      view: card
---
