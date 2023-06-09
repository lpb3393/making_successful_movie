![director shot](https://github.com/lpb3393/making_successful_movie/blob/main/images/director_shot.jpeg)




# Making a Successful Movie

**Author:** Laura Brown
***



## Overview

The success of a movie can be measured in different ways, but it typically depends on a combination of factors. A successful movie is one that resonates with audiences, receives critical acclaim, and generates substantial revenue. A movie that earns high box office revenue is generally considered successful because it indicates that the movie was well-received by audiences and generated significant interest. But what is the typical budgets of movies that are considered "successful"? What time of year are people most likely to see a movie? There are many factors that determine the success of a movie but by using descriptive analysis we can establish what will increase any movie’s chance for success.



## Business Problem

Given information about movies that have previously been released, we want to know what factors we can pinpoint that will increase our chance for financial success in the cinematic space. The most important being, when people are most likely to go see a movie in theaters, what movies budgets typically have a high Return of Investment and what genre on average generates the most domestic gross revenue. There are other factors that can determine the success of a movie but when entering the movie production business, Microsoft should be most concerned with the financial aspects to establish themselves amongst those already dominating the field.  

![movie items](https://github.com/lpb3393/making_successful_movie/blob/main/images/Movie_Items.jpg)

## Data Understanding

The data I am using to perform this analysis is from IMDB, the most robust website/database when it comes to information about movies. I am going to take each movie’s domestic gross and combined it with other tables to see how it is correlates to these other important aspects of a movie. By looking at each movies release date, its genre and how much each movie spent on creating it, I will be able to answer important questions in regards with how to have the highest possible chance of a successful movie.



## Data Exploration

First, I imported all the necessary libraries I will need for this analysis. I wanted to be able to look at all of the files provided and find the important information we need to ultimately answer the business question. Once I established the factors, I felt were important in creating a successful movie and found information I can use, I then found mutual columns between tables to prepare for data cleaning.



## Data Preparation


The first thing I want to consider is what genre of movie typically has the highest domestic gross value. In order to do that I joined the "movie_basics" table and the "movie_ratings" table based on the 'movie_id" column, that way I could have the genre and the title of that movie in the same table. After that, I separated each movies' genre into its own row and removed columns in the table I did not need. 


The second question that needed to be asked is, how much should a production company spend to get the highest return on investment? I took the total domestic gross for each movie and subtracted it with its production budget to get the ROI. Then by compared it again to each movies production budget, it provided insight for an ideal cost to produce a movie.


Lastly, I wanted to know what time of year do people typically see movies or what month of the year makes generates the most profit? By looking and when each movie was release and taking the average earned per month, I was able to see which month will increase the likelihood of having a financially successful movie.



## Data Modeling


To best analyze this data and see what genre is the most successful at the box office, I want to use a bargraph to directly compare genre and domestic gross. After using code to determine that top five producing genres and plotting them, it's interesting to see who the top earners are. In the given dataset, each movie has one to three genre types listed, but it seems that Sci-Fi and adventure are the most common and successful. When trying to determine what will make a movie succeed, the goal is to first make a type of movie that people will enjoy the most. 


![genre](https://github.com/lpb3393/making_successful_movie/blob/main/images/Top_5_Genre.JPG)



Setting an appropriate movie budget is crucial for maximizing ROI because it can directly affect the financial success of the film. If a movie is made with a budget that is too high, it may be difficult to recoup the costs through box office sales or other revenue streams. On the other hand, if a movie is made with a budget that is too low, the quality of the film may suffer, which could result in poor reviews and low box office sales. To determine what budget is likely to yield results I calculated Return on Investment for each movie and directly compared it to that movies production budget. From the graph you can see that budgets of 30 to 35 million produce the best results.


![production budget](https://github.com/lpb3393/making_successful_movie/blob/main/images/Production_Budget.JPG)



![overall domestic gross comparison](https://github.com/lpb3393/making_successful_movie/blob/main/images/Overall.JPG)



The time of year a movie is released can be important for several reason. For example, studios often release blockbusters during the summer months when more people have free time to go to the movies. Additionally, some movies are released during the holiday season to take advantage of the increased spending on entertainment during that time of year. But which month typically comes out on top financially? By calculating the mean domestic gross for each month and having python choose the top five earners, this bar graph shows a near tie between May and June.


![month of release](https://github.com/lpb3393/making_successful_movie/blob/main/images/Top_5_Months.JPG)



## Evaluation

Genre:
From looking at this graph, Sci-Fi is the clear leader in domestic gross. In the data provided, each movie listed typically had multiple genres given, so it is possible that Sci-fi was alongside another category. But going off this data and the results from this analysis, choosing a combination of the top genres would be likely to give positive results. 

Production Budget: After comparing production budget to return on investment, most films spend around 10 million dollars, while not breaking even. For optimal return, it looks like movies need to spend about 40 million to earn the highest domestic gross.

Month of Release:
There seems to be a near tie between May and June for domestic gross earned at the box office. This is aligned with what I initially predicted as kids are out of school and people have more time for entertainment.



## Conclusions

After completing this analysis there are three clear recommendations for making sure the film that is produced is successful:
First, creating a movie that is both classified as Sci-Fi and Adventure would ensure that it is a hit at the box office. 
Next, releasing the movie in May would generate the most profit by optimizing the maximum number of people that can go to the theaters to see it.
Lastly, to capitalize on the highest possible ROI, the budget for this film needs to be approximately 40 million dollars.


Questions to consider:

Would movie rating (PG-13, R, etc.) affect the domestic gross for each genre? Would a dataset that did not have Null values change the results? Who determines what combinations of genres a movie is?

To improve this project in the future, it would be helpful to determine what movie rating is the highest grossing and most popular. The rating could make a movie drastically different and more widely accessible if it was rated G rather than R but would be helpful to see if on average it made it more succesful. Also, finding which actors that have more of a draw to get people in theaters would be very beneficial information to have.



## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/lpb3393/making_successful_movie/blob/main/making_successful_movie.ipynb) or review the [presentation](https://github.com/lpb3393/making_successful_movie/blob/main/Making%20A%20Successful%20Movie%20Presentation.pdf)


## Repository Structure

```
├── images
├── .gitignore
├── Making A Successful Movie.pdf
├── ReadMe.md
└── making_successful_movie.ipynb
```
