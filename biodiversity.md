---
title: "Use Your Creativity: Biodiversity and Redlining Bar Chart"
teaching: 15
exercises: 1
---



::::::::::::::::::: instructor

### INSTRUCTOR NOTE (`on creativity in this exercise`)

test of new text

Part of this work will invovle creative attempts at making changes to data visualizations. While the first few exercises are intended to help students become familiar with the basic steps, the final independent exercise is meant to introduce more gaps. If possible, emphasize to students that if they struggle on the final independent exercise it is not about making a perfect graph, but learning how to make changes on their own terms.

::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::: questions 

- How can I read tabular data to plot a bar graph in R?
- How can I use ggplot to organize and format a bar graph in R?
- What are the characteristics of Du Bois data visualizations?
- How can I maintain a reproducible record of my data visualizations?
- How can I use color to improve accessibility of data visualizations?
- How can I engage my own creativity in data visualizations?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Create bar graph variations based on historical and contemporary tabular data.
- Develop basic R code to create bar graphs.
- Examine the characteristics of the data visualization from 1900 exhibitions.  
- Use transparent, legible, and shareable record of how you created your own unique data visualizations.
- Create an exported HTML file of your completed Notebook that your instructor may ask you to submit.
- Differentiate color usage to improve legibility of findings from tabular data.
- Implement your own creative ideas through data visualization.

::::::::::::::::::::::::::::::::::::::::::::::::

### Black Literacy After Emancipation

<div>
<img src="https://camo.githubusercontent.com/c38273c834787fc9ea22aadc1d980f0ff28a627bf4d3852dd4034b9f75fcc4bd/68747470733a2f2f6769746875622e636f6d2f4869676865724564446174612f44752d426f69732d5354454d2f626c6f622f6d61696e2f72656164696e67732d696d616765732f6f726967696e616c2d706c6174652d34372e6a70673f7261773d74727565" width="700" />
</div>

::::::::::::::::: callout

This interactive exercise is inspired by the annual #DuBoisChallenge. The #DuBoisChallenge is a call to scientists, students, and community members to recreate, adapt, and share on social media the data visualzations created by W.E.B. Du Bois and his collaborators in 1900. Before doing the interactive exercise, please read this article about the Du Bois Challenge: https://nightingaledvs.com/the-dubois-challenge/

:::::::::::::::::

### How can I input tabular data to plot a bar graph in R?

The first step for data visualization in R is to read data into an R dataframe. This is like double clicking a file to open it in other computer programs. But with R, we use code.

For this exercise, we're going to read in data from a website. And we're going to place the data into a dataframe named d_literacy_country.

The R code to do this uses an ```<-``` arrow pointed at the name of the data frame and a read.csv function command followed by the web address within paraentheses where a csv (comma separated values) data file is located. It looks like this:

```
d_literacy_country <- read.csv("web_address_with_data/data_file_name.csv")
```

:::::::::::::::::::::: challenge

After writing this code, we can write the name of the data frame d_literacy_country again on a separate line. This will list all of the data in the data frame.

To do this yourself, replace the ____ portion of the code below to add the read function and then press the code below to add the read function and then press the above.

::::::::::::::::::::::

### Creating a Bar Graph
After successfully listing the data above, you should be able to see that it has data in two columns. Each column is a variable:

country is a country name for 10 countries with Black people in the U.S. treated as a country.
illiteracy containts percent of people in each country who are illiterate.
As a first step, we will create a bar graph of the data using the shortest code possible. The code will:

repeat the code below that we wrote above to read in the Du Bois illiteracy data.
add a line of code to load the ggplot2 package of functions into our Library that we will use to generate our graph: library(ggplot2)
Add a line of code to tell Jupyter and R that we want the width and height of the graph to have the same ratio that Du Bois used, 22 inches wide by 28 inches tall, with each divided by 2 so that it doesn't display too big: options(repr.plot.width=22/3, repr.plot.height=28/3)
Finally, we add a ggplot function followed by open parenthese to tell R that we will plot data from the d_literacy_country data frame with an "aesthetic mapping" aes specification that maps one column of data on the x axis and another column of data on the y axis.
After the close parentheses that tells ggplot we want to plot d_emancipation_dubois data with one variable on the x axis, and another on the y axis, we add a + and then a new line of code geom_col() that tells ggplot we want a bar graph based on summary statistics in the dataframe.
After looking at Du Bois' version of the graph above, replace the _____ characters in the code cell below to plot the correct variable on the x-axis and the correct variable on the y-axis.

::::::::::::::::: prereq

### JUPYTER LAB NOTEBOOK

If you are using Jupyter on the Du Bois cloud for this exercise (no installation required),
you can open the Notebook for this exercise on your web browser [here](https://dubois.2i2c.cloud/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FHigherEdData%2FDu-Bois-STEM&urlpath=tree%2FDu-Bois-STEM%2Fr_literacy_biodiversity_dubois.ipynb&branch=main)

To continue the exercise using R Studio on your own computer, continue below.

::::::::::::::::::::::::

### You will learn how to use the *R* statistical programming language by creating two graphs:

1. You will recreate Du Bois' visualization of Black illiteracy rates in the US compared to illiteracy rates in other countries. Du Bois created the visualization in 1900.

2. You will reproduce Du Bois' visualization using data on Black college attainment in the US today. This aligns with how Du Bois saw mass education as one important strategy for furthering and deepining emancipation for Black Americans and others.

3. An important context of Du Bois's graph of Black illiteracy is that literacy was illegal for enslaved people in the U.S. until emancipation and the Confederacy's defeat during the Civil War. Illiteracy then declined rapidly as Black Americans sought to empower themselves through education. The Du Bois plotted this decline in illiteracy among Black residents in the state of Georgia in the figure below. They used decennial US census illiteracy rates for Georgia from 1860 to 1890 that are available **[here](https://babel.hathitrust.org/cgi/pt?id=njp.32101025729177&seq=49)**. They likely wrote "50%?" for the 1900 illiteracy rate because the Census did not publish 1900 illiteracy rates (available **[here](https://www2.census.gov/library/publications/decennial/1900/bulletins/demographic/8-negroes-in-us-part-1.pdf)**) until several months after the Paris Exposition.

<div>
<img src="https://github.com/ajstarks/dubois-data-portraits/blob/master/plate14/original-plate-14.jpg?raw=true" width="700" />
</div>

### How to use this interactive **Jupyter Notebook**

If you know how to use R on your own computer with R Studio you can copy, paste, and edit code in R Studio to do the exercise. If you have Jupyter Lab, you can also download this Notebook to use it on your own computer. You can download the Notebook or view a non-interactive version of this Notebook by clicking **[here](https://github.com/HigherEdData/Du-Bois-STEM/blob/main/r_literacy_dubois.ipynb)**.

::::::::::::::::::::::::::::::::: challenge

### Coding in Jupyter Lab Notebooks

To use this Notebook interactively, Grey cells in the *Notebook* like the one below are **code cells** where you will write and edit **R** Code. To try it out:

1. Click your cursor on the grey cell below. After you click on it, it will change to white to indicate you are editing it.
2. After you click on the cell below and it turns white. Type 2+2 to use R as a calculator.
3. After typing 2+2, click the play button at the top of the notebook page.

::::::::::::::::: hint

### HINT (`hint`)

If you are getting an error, make sure there are no spaces or other symbols between 2+2.

::::::::::::::::::::::

::::::::::::::::: solution

### SOLUTION

If everything is working correctly, you should be given a reported value of 4.

Here is the code executed unsuccessfully because it includes an equal sign.

``` r
2+2=
```

``` error
Error in parse(text = input): <text>:2:0: unexpected end of input
1: 2+2=
   ^
```

Here is the code executed successfully.


``` r
2+2
```

``` output
[1] 4
```


::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
