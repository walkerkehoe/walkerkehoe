---
title: Home
sections:
- type: heroblock
  template: heroblock
  title: Hi, I'm Walker.
  section_id: hero
  component: hero_block.html
  content: 'I''m a well-rounded engineer currently pursuing a Master''s in Aeronautics
    & Astronautics at Stanford. I spent the year before volunteering at a nonprofit
    in South Africa. Before that I worked in consulting building machine learning
    algorithms. '
- type: portfolioblock
  template: portfolioblock
  title: Projects
  section_id: latest-projects
  component: portfolio_block.html
  subtitle: ''
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
