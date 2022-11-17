---
author: Aidan Gildea, Jessie Bierschenk, Julia Mitchell, Naomi Rubin, and Gaurav Sirdeshmukh
categories:
- Data Science
- R Shiny
date: "2022-04-30"
draft: false
layout: single
links:
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/Sta323-Sp22/final_proj_squAdjusted_R2
subtitle: STA 323 - Statistical Computing
tags:
- hugo-site
title: Duke Basketball R Shiny Database
---

## Introduction

This year, Duke witnessed a historic basketball season, with it being Coach K's last season and playing so well throughout the season and March Madness. Therefore, we decided to make our final project all about Duke men's basketball statistics. Our project scrapes Duke men's basketball data, about both the team and individual players, from the goduke.com website. We then created a Shiny app to present this data and allow users to look up individual player stats and access different summary statistic reports. The app incorporates visualizations relevant to team and individual data. Our goal is to create an app that provides the user with informative and accessible insights into team and player performance, while also being reproducible for future seasons.

## Methods / Implementation

The first half of our project is dedicated to scraping and cleaning the Duke
Men's basketball data from the 2021-2022 season. We scraped this data from
`https://goduke.com/sports/mens-basketball/stats`. For our project, we wanted to
scrape that data on the team statistics and overall individual statistics. We 
used selector gadget and inspected the pages to determine the best way to scrape 
the data. We were able to find the xpath by inspecting the pages and hovering 
over the element we wanted to scrape. We used xpaths that returned all of the
data in html format for the "Team" and "Individual" pages. After scraping the
data we had to clean it.

We split the team and individual statistics into two separate data frames. For 
the team statistics data frame, we had to clean the data in multiple ways. First,
we added a variable "type" to indicate which category, (i.e. "Scoring", 
"Shooting","Rebounding", etc.) the statistic falls under. We populated this
variable for every statistics. We also renamed poorly labelled columns
and cleaned the output of the rows. 

For the individual statistics data frame, we also had to clean the data. First,
we renamed the columns.The columns specify the statistic, unit, and the category 
the statistic falls into ("minutes", "scoring", and "rebounds") if it is a repeated 
column name (i.e. "AVG"). We also fixed the rows so that the "Player" column
returns the row in a better format. Lastly,the html contains "conference", 
"scoring", and "average" statistics in addition to "overall" but we only 
included the "overall" data. We filtered the data frame for the overall data
and removed all rows that were not in that data set.

Then we developed our Shiny app. First, the user can interact with a drop down menu on the side panel and choose to view team stats or choose to view individual player stats. If the user chooses to view individual player stats, they then can interact with another drop down menu and choose from the roster which player's stats they would like to view. Upon pressing the action button, the main panel will produce the output corresponding to the appropriate selection. In the main panel, users can toggle between two panels, one for the overall stat line (in table format) or a summary visualization (in graph format). The content of the main panel will update dynamically when switching between the two tabs; however, if changing the input for the team/individual drop down, the user must press search again. The overall stat line is a table of statistics, either about the team's performance or an individual player's performance depending on the user's selection in the side panel. The summary visualization tab features a unique plot for team performance and a dynamic plot for individual performance. The graph for team performance allows users to compare the team's per game average statistics (ie. points per game, rebounds per game). The graph for individual performance allows users to compare the players' FG%, FT%, and 3PT%, with the player of interest's data points highlighted. Altogether, the app is an intuitive and east-to-use tool for users who want to explore the Duke Men's Basketball Team's performance during the 2021-2022 season. 

## Discussion & Conclusions

After scraping the data and creating a Shiny app, we feel that we have presented Duke men's basketball statistics in an informative, interactive, and user-friendly way. The app allows users to filter the data easily and look at a variety of different summary statistics. Although we are happy with the way that our app turned out, we feel that there is much we could expand upon in the future.

In the future, we would be interested in expanding upon our project by scraping more data and adding more elements to our Shiny app. This could look like scraping data from previous years, scraping data about other teams, adding more visualizations to our Shiny app, and generally expanding the scope of our app.

One of our main objectives was to ensure that our code is reproducible and generalizable. Every ACC school uses the same website for their athletics pages, and as such, team and individual data is formatted essentially identically. We could expand this app from just Duke basketball, to all of the ACC - and do so without having to worry about data frames being structured differently. This could open the door to many new visualizations and for comparisons between teams and our app would become more of an analytical tool than it currently is. An alternative to this would be to implement a fileInput() where the user can scrape and import data themselves. However, doing this scraping and cleaning ourselves and updating the app’s functionality to allow for team selection would benefit the user experience.

### Data Wrangling: Team Statistics

Explore our code on [Github](https://github.com/Sta323-Sp22/final_proj_squAdjusted_R2).