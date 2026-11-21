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
      # Buttons are in the home-actions section below (View Experience + View CV side by side)
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
    id: home-actions
    content:
      title: ''
      text: |-
        <div class="home-cta-row not-prose">
          <a class="home-cta home-cta--primary" href="/experience/">View Experience</a>
          <a class="home-cta home-cta--secondary" href="/cv/Savvas-Panagi-CV.pdf" target="_blank" rel="noopener">View CV</a>
        </div>
    design:
      columns: '1'
  - block: markdown
    content:
      title: 'Welcome'
      subtitle: ''
      text: |-
        Welcome to my website! From an early age, I recall being passionate about programming, troubleshooting computer hardware problems, and experimenting with every electrical appliance that came my way. This passion drove me to study electrical and computer engineering.

        I am currently an Industrial PhD Student at the Electricity Authority of Cyprus and a Part-time Researcher at the Sustainable Power System Lab of the Cyprus University of Technology.

        On this website I share research updates, projects, and selected notes from my learning journey across power systems, programming, automations, and related topics. You can also [download my CV](/cv/Savvas-Panagi-CV.pdf).
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Latest Publications
      count: 4
      order: desc
      filters:
        folders:
          - publications
      archive:
        enable: true
        text: All publications
        link: /publications/
    design:
      view: article-grid
      columns: 5
      fill_image: false
      show_date: true
      show_read_time: false
      show_read_more: false
  - block: collection
    id: news
    content:
      title: Latest Articles
      subtitle: ''
      text: ''
      page_type: blog
      count: 2
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
      view: article-grid
      columns: 2
      fill_image: false
      show_date: true
      show_read_time: false
      show_read_more: false
      spacing:
        padding: [0, 0, 0, 0]
  - block: collection
    id: talks
    content:
      title: Timeline
      text: Conferences, workshops, secondments, and milestones. See the full [Timeline](/events/).
      filters:
        folders:
          - events
        exclude_future: false
      count: 2
      order: desc
    design:
      view: card
  - block: collection
    id: projects
    content:
      title: Projects
      text: Selected research projects. See all [Projects](/projects/).
      filters:
        folders:
          - projects
      count: 2
      order: desc
    design:
      view: card
      fill_image: false
  - block: resume-skills
    id: skills
    content:
      title: Skills
      username: me
  # - block: resume-languages
  #   id: languages
  #   content:
  #     title: Languages
  #     username: me
  # - block: resume-experience
  #   id: experience
  #   content:
  #     username: me
  #   design:
  #     date_format: 'January 2006'
  #     is_education_first: false
---
