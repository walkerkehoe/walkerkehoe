+++
content_img_path = "/images/Screen Shot 2020-04-02 at 9.43.55 AM.png"
date = 2019-06-01T07:00:00Z
layout = "project"
subtitle = ""
thumb_img_path = "/images/Screen Shot 2020-04-02 at 9.41.32 AM.png"
title = "NGO Social Performance Dashboard"

+++
### Overview

In between my time in consulting and graduate school, I spent a year volunteering for the Small Enterprise Foundation, a financial inclusion nonprofit in South Africa. One of my projects there was to build a tool that could help track social outcomes of the organization’s microfinance lending program. You can play with an interactive version of the tool [here](https://walkerkehoe.shinyapps.io/socialperformance/).

### Defining Metrics

As a bank, they were good at tracking financial performance, using measures like rate of repayment and total outstanding portfolio. Social outcomes were just as important to them, but proved more challenging to measure organization-wide because many of these metrics are difficult to quantify. Traditionally this was done through one off audits or aggregation of anecdotes from client interviews. We started the project by taking an inventory of all the data the organization was collecting on its clients. With this list we were able to brainstorm some high level social metrics that we knew were trackable:

* Number of clients
* Client poverty assessment
* Amount client has in savings
* Client business value

### Telling the Story

The organization wanted a dashboard that would update automatically and could be used by everyone from field officers to the board of directors. They also wanted something that would be inexpensive to maintain. Given these requirements, I decided to build the tool in R Shiny. We tested a number of designs before settling on the final iteration which features a snapshot on the front page with stoplight colors and arrows that add meaning to the numbers being displayed. There's a slider on the side that enables the user to step backwards in time to compare current and historical performance. For a deeper dive into the metrics, there are five graphs that filter by date and geographic location. 