---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: View Experience
        url: experience/
      headings:
        about: About me
        education: Education
        interests: Interests
    design:
      # Use the new Gradient Mesh which automatically adapts to the selected theme colors
      background:
        gradient_mesh:
          enable: true

      # Name heading sizing to accommodate long or short names
      name:
        size: md # Options: xs, sm, md, lg (default), xl

      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  - block: markdown
    content:
      title: 'Welcome'
      subtitle: ''
      text: |-
        Welcome to my website! From an early age, I recall being passionate about programming, troubleshooting computer hardware problems, and experimenting with every electrical appliance that came my way. This passion drove me to study electrical and computer engineering.

        I am currently an Industrial PhD Student at the Electricity Authority of Cyprus and a Part-time Researcher at the Sustainable Power System Lab of the Cyprus University of Technology.

        On this website I regularly share content that I find useful throughout my learning journey. The blog covers topics such as Power Systems, Programming, Automations, Arduino, Mathematics, and related subjects.
    design:
      columns: '1'
  - block: collection
    id: news
    content:
      title: Latest Articles
      subtitle: ''
      text: ''
      page_type: blog
      count: 6
      filters:
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ''
      offset: 0
      order: desc
    design:
      view: card
      spacing:
        padding: [0, 0, 0, 0]
  - block: resume-skills
    id: skills
    content:
      title: Skills
      username: me
  - block: resume-experience
    id: experience
    content:
      username: me
    design:
      date_format: 'January 2006'
      is_education_first: false
---
