---
title: Home
sections:
- type: heroblock
  template: heroblock
  title: Hi, I'm Stackbit Exto Portfolio Theme.
  section_id: hero
  component: hero_block.html
  content: This section can contain a subtitle or tagline. The recommended length
    is one to three sentences, but can be changed as you prefer.
- type: portfolioblock
  template: portfolioblock
  title: Recent Work
  section_id: latest-projects
  component: portfolio_block.html
  subtitle: An optional subtitle of the section
  layout_style: mosaic
  num_projects_displayed: 6
  view_all_text: View All
  view_all_url: portfolio/index.html
- type: postsblock
  template: postsblock
  title: Latest from the Blog
  section_id: latest-posts
  component: posts_block.html
  subtitle: An optional subtitle of the section
  num_posts_displayed: 2
  actions:
  - label: View Blog
    url: blog/index.html
layout: home
menu:
  main:
    weight: 1

---
