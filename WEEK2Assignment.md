---
title: "Week 2 Assignment: Popular Tourist Sites in the US"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## Instructions

Create a web page using R Markdown that features a map created with Leaflet. Host your webpage on either GitHub Pages, RPubs, or NeoCities.  
Your webpage must contain the date that you created the document, and it must contain a map created with Leaflet. We would love to see you show off your creativity!

## Review criteria
The rubric contains the following two questions:
  1. Does the web page feature a date and is this date less than two months before the date that you're grading this assignment?
  2. Does the web page feature an interactive map that appears to have been created with Leaflet?

## Map
Hover to the spots and link to the website of these fun attraction sites!

```{r, echo = F}
library(leaflet)
tourSpot <- data.frame(lat = c(28.417839, 40.689249, 37.819929, 38.733081, 37.865101),
                       lng = c(-81.581235, -74.044500, -122.478255, -109.592514, -119.538329))
tourSites <- c(
  "<a href='https://disneyworld.disney.go.com/'>Disney World</a>",
  "<a href='https://www.nps.gov/stli/index.htm'>Statue of Liberty</a>",
  "<a href='http://www.goldengatebridge.org/'>Golden Gate Bridge</a>",
  "<a href='https://www.nps.gov/arch/index.htm'>Arches National Park</a>",
  "<a href='https://www.nps.gov/yose/index.htm'>Yosemite National Park</a>"
)

tourSpot %>% leaflet() %>% addTiles() %>% addMarkers(popup = tourSites)
```
