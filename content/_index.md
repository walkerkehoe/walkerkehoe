---
title: Home
sections:
- type: heroblock
  template: heroblock
  title: Hi, I'm Walker.
  section_id: hero
  component: hero_block.html
  content: 'Well-rounded engineer. Former consultant. '
- type: portfolioblock
  template: portfolioblock
  title: Projects
  section_id: latest-projects
  component: portfolio_block.html
  subtitle: ''
  layout_style: mosaic
  num_projects_displayed: 4
  view_all_text: View All
  view_all_url: portfolio/index.html
- type: postsblock
  template: postsblock
  title: Latest from the Blog
  section_id: latest-posts
  component: posts_block.html
  subtitle: Check out what I'm working on.
  num_posts_displayed: 2
  actions:
  - label: View Blog
    url: blog/index.html
layout: home
menu:
  main:
    weight: 1

---
