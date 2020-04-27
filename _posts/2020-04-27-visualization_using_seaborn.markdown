---
layout: post
title:      "Visualization using Seaborn"
date:       2020-04-27 17:14:18 -0400
permalink:  visualization_using_seaborn
---


The ultimate goal of any data scientist is to bring any data to life.  Pure numbers on a screen or somewhere in a database is not useful, unless one can clearly visualize it and discern a pattern. 

Data visualization helps in communicating results clearly to a general audience. Visualization also helps in bringing out new propositions or follow up steps in a project. 

For our module 1 project, I had to use Seaborn to display my results. I primarily used histograms as they give a good overview of all the possible data points of interest, and their frequency. 

The code below, displays a plain monochromatic histogram without the rich color range of seaborn palette.

 
```
f, ax = plt.subplots(figsize=(20,20))
sns.axes_style('whitegrid')
sns.set_context('talk') 
sns.barplot(x_genre_count, y_genre_count, palette='Blues_d')
plt.title('Popular Genres for Non-English Films', fontsize=30)
plt.xticks(rotation=45)
plt.ylabel('Number of Movies 2010 - present', fontsize=25)
plt.xlabel('Genre', fontsize=25) 
plt.show()

```
 


Even though the chart serves its purpose, the choice of color from the Seaborn color palette was not fully applied.

![Monochrome_Pop_Genre](images/Monochrome_Pop_Genre.png)


With a slight change in the visualization code, as displayed below...., 

```
f, ax = plt.subplots(figsize=(16,12))
sns.axes_style('darkgrid')
sns.set_context('talk') 
sns.barplot(x_genre_count, y_genre_count, palette='Paired')
plt.title('Popular Genres for Non-English Films', fontsize=30)
plt.xticks(rotation=45)
plt.ylabel('Number of Movies 2010 - present', fontsize=25)
plt.xlabel('Genre', fontsize=25) 
plt.show()

```
 

...you can see how the histogram comes to life on the same presentation.


 ![Non-English_Genre](/images/Non_English_Genre.png)



Such a vivid graphics goes a very long way in helping your audience grasp the essence of your presentation and make decisions much faster.
You can read more here https://towardsdatascience.com/10-viz-every-ds-should-know-4e4118f26fc3 about other visualization methods for a data scientist.

