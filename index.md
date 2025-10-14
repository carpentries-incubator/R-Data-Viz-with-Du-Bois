---
site: sandpaper::sandpaper_site
---

<div>
<img src="https://github.com/HigherEdData/Du-Bois-STEM/blob/main/readings-images/original-plate-47.jpg?raw=true" width="700" />
</div>

This is a lesson for learning how to create scientific data visualizations in R.
The lesson uses examples from charts created by Black social scientist W.E.B. 
Du Bois and a diverse team of collaborators for the 1900 Paris World Expo.

The Du Bois team's visualizations were state of the art in 1900, using most of
the major chart types still employed across the sciences and engineering today.
The Du Bois charts provided some of the first widely accessible scientific 
analyses to refute false, biologically based theories of racial inequality. For
their innovative analyses, beauty, and historical importance, the original 
hand drawn charts are preserved in the U.S. Library of Congress.

The lesson is designed for learners with little or no programming experience. The
entire lesson can be taught in a two day workshop. Alternatively, selected
episodes from the lesson can be taught over a period of around 3 hours of lecture
and lab within a STEM course (see
[Instructor Notes](https://github.com/carpentries-incubator/R-Data-Viz-with-Du-Bois/instructor/instructor-notes.html)
for suggested lesson plans). The lesson starts with the social and scientific
context in which Du Bois created the visualizations. The lesson then introduces
key chart types for different kinds of data and visualization best practices. 
Multiple episodes are then offered for recreating or adapting selected Du Bois
charts with modern data, including bar graphs and statistical maps.

This lesson part of a series of **[STEM Data Visualization and Du Boisian Methods](https://github.com/HigherEdData/Du-Bois-STEM/tree/main)**
modules for learning data visualization in R, Python, Stata, and more. 
Development and testing of the modules is funded by the National Science Foundation.

## Overall Lesson Learning Objectives

Each episode of the lesson has more specific learning objectives. The overall
lesson learning objectives are:

* Understand the social and scientific context of visualizations as a process of
scientific discovery (observation, hypothesis formation, data collection, analysis).
* Practice creative and visual thinking as valuable methods for scientific
discovery and communication.
* Comprehend major chart types (pie bar, bar chart, line chart, statistical map)
and their suitability for different levels of measurement and multivariate
relationships.
* Apply visualization best including accessible design and data story telling.
* Create and modify a Du Bois chart using R to experience the value of coding
to reproduce and adapt data visualizations in STEM.

::::::::::::::::::::::::::::::::::::::::::  prereq

## Getting started

**This lesson assumes no prior knowledge of the skills or tools.**

There are three ways to engage with the coding portions of this lesson:

1. Use Jupyter Notebooks with an R Kernel on the Du Bois Cloud Jupyter Hub.
2. Use Jupyter Notebooks with an R Kernel on students' own computers.
3. Use R Studio on students' own computers.

The Du Bois Cloud option can be done with any web browser and requires no
installation. We recommend that option if students are not expecting to do further
data visualization using R for their courses or research.

#### Prerequisites for using students' own computers

For options 2 and 3 using students' own computers, follow the directions in the 
"[Setup](setup.html)".

For option 2, students will need **Jupyter Lab**, **R**, and a Jupyter **R Kernel**.

For option 3, students will need and **R** and **RStudio**.
<br>To most effectively use these materials, please make sure to install
everything *before* working through this lesson.


::::::::::::::::::::::::::::::::::::::::::::::::::

**Resources**
1. R-Social Sci Index Reference
- https://github.com/datacarpentry/r-socialsci/blob/main/index.md

2. Componente Guide for Building Out Formatting Boxes for GitHub
- https://carpentries.github.io/sandpaper-docs/instructor/component-guide.html

# Context

- Learning Objective 1: Explain why data visualization and creativity are vital tools in scientific research.
- Learning Objective 2: Comprehend why data visualization historically originated in the social sciences, including Du Bois' analyses that challenged false biological theories of racial inequality. 
- Learning Objective 3: Understand how Du Bois used visualizations to accessibly communicate findings to a broad audience.
- Learning Objective 4: Undrstand the benefits of a "team science" approach similar to that used by Du Bois.

# Implement: Create a Du Bois Bar Graph with R - Biodiversity and Redlining Data

- Learning Objective 1: Create bar graph variations based on historical and contemporary tabular data
- Learning Objective 2: Create R code that generates consistent and accurate visualizations based on different tabular data sets
- Learning Objective 3: Maintain a transparent, legible, and shareable record of how you created your own unique data visualizations
- Learning Objective 4: Implement your own creative ideas through data visualization based on tabular data sets
- Learning Objective 5: Re-create historical data visualizations into a digital environment with R coding
- Learning Objective 6: Improve the legibility and accessibility of data visualizations
- Learning Objective 7: Use ggplot to visualize tabular data as a function within R
- Learning Objective 8: Use color to improve legibility of findings from tabular data


[workbench]: https://carpentries.github.io/sandpaper-docs

