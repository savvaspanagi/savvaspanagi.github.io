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
      # Bio + two CTAs under About me (theme supports only one native button)
      text: |-
        I am a passionate researcher specializing in energy power systems. My work focuses on the operation and flexibility of active distribution networks, including electric vehicles, heat pumps, and related energy technologies.

        From an early age, I have been passionate about programming, troubleshooting computer hardware, and experimenting with electrical systems — a curiosity that led me to study electrical and computer engineering.

        I am currently an Industrial PhD Candidate at the Electricity Authority of Cyprus and a Part-time Researcher at the Sustainable Power System Lab of the Cyprus University of Technology, where I combine academic research with industrial practice.

        <div class="home-cta-row home-cta-row--inline not-prose">
          <a class="home-cta home-cta--primary" href="/experience/">View Experience</a>
          <a class="home-cta home-cta--secondary" href="/cv/Savvas-Panagi-CV.pdf" target="_blank" rel="noopener">View CV</a>
        </div>
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
