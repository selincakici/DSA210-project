
# DSA210 Project– How Does My Academic Life Affect My Watching Habits?

## Project Proposal
In this project, I will be analyzing the relationship between my watching habits and my academic life. I will explore how academic workload changes several aspects of my watching habits such as the duration, genre, ratings, language of the movies I watch.

## Motivation 
As a cinephile I’ve realized my watching habits change when the semester begins. With the workload of the semester (exams, quizzes, assignments) I start to watch less movies or I watch something lighter. During semester I tend to avoid long or complex movies. With this project, I aim to explore this change not only in terms of the total time, but also what, how and when I watch. 


## Data and Collection  
I will examine duration, year, country, language, origin, ratings, date I watched for the movies. 

And for my academic life I plan to use the exam dates, homework dates and their frequency. I will enter these data manually into a CSV file to represent my academic workload level.

I regularly log the movies I watch on Letterboxd so for the movies I watch I will use my data from Letterboxd.

However, Letterboxd only gives me Date, Year, Rate, Name. To get the duration, genre, language,average ratings,cast of the movies I watch , I will use TMDB (The Movie Database) dataset which contains this information for movies. 

I created an academic workload file to get the dates of my exams,quizzes and homeworks.

## Datasets
**academicworkload:** Date, Course, Type, Importancy.  
**diary:** Date, Name, Year, Letterboxd URI, Rating, Rewatch, Tags, Watched Date.       
**allwatched:** Title, MyRating, MyWatchedDate, Year, Genres, Runtime ,TMDB_Rating, Language, ReleaseDate, Popularity, Cast. 

## Hypotheses
### Academic Workload and Movie Watch Time
**Null Hypothesis (H₀):** Weekly academic workload has no meaningful influence on the number of movies I watch during that week. The number of movies I watch in a week are random and are not affected by the the changes in academic workload.

**Alternative Hypothesis (H₁):** Weekly academic workload has a significant influence on my movie watching behaviour. Specifically, as academic workload increases, the number of movies I watch per week tends to decrease in a consistent pattern, indicating a measurable behavioral response to rising academic pressure.

### Academic Workload and Movie Langauges
**Null Hypothesis (H₀):** The distribution of movie languages watched during high-workload weeks is the same as the distribution of languages watched during low-workload weeks.
In other words, academic workload does not influence the languages of the movies selected.

**Alternative Hypothesis (H₁):** The distribution of movie languages watched during high-workload weeks is significantly different from the distribution observed during low-workload weeks.This implies that academic workload affects language selection, meaning certain languages may be more or less likely to be chosen depending on the level of workload.

### Academic Workload and Genres
**Null Hypothesis (H₀):** The distribution of movie genres watched during high-workload weeks is the same as the distribution of genres watched during low-workload weeks.
In other words, academic workload does not influence the types of movie genres selected.

**Alternative Hypothesis (H₁):** The distribution of movie genres watched during high-workload weeks is significantly different from the distribution observed during low-workload weeks.
This implies that academic workload affects genre selection, meaning certain genres may be more or less likely to be chosen depending on the level of workload.

## Hypothesis Testing Results
### Academic Workload and Movie Watch Time
Based on the results of the two-sample t-test (t = −2.58, p = 0.039), the p-value is below the significance level 0.05. Therefore, the **null hypothesis (H₀) is rejected**. This means that weekly academic workload  have a significant influence on the number of movies I watch per week. Consistent with the alternative hypothesis (H₁), higher workload weeks are associated with substantially fewer movies watched.

### Academic Workload and Movie Langauges
The chi-square test examining whether academic workload influences the language of movies watched shows no statistically significant association between the two variables (χ² = 2.07, p = 0.96). Because the p-value is higher than the 0.05 significance level, the null hypothesis (H₀) **cannot be rejected.** This means that the distribution of movie languages is essentially the same in both high-workload and low-workload weeks. Academic workload does not influence which languages I choose to watch. 

### Academic Workload and Genres
The test results show no statistically significant association between weekly workload level and genre selection (χ² = 9.63, p = 0.141). Because the p-value is bigger than the  0.05 threshold, the null hypothesis (H₀) **cannot be rejected.**
This means that the distribution of genres is essentially the same in both high-workload and low-workload weeks.The types of genres I choose remain consistent regardless of academic pressure.

## Machine Learning
I applied machine learning methods to investigate the following questions:
How much academic workload I will have on a weekly basis
How many movies I will watch each week
The total distribution of movie genres I am expected to watch during the Spring semester
The distribution of movie languages I am expected to watch during the Spring semester

To estimate my weekly academic workload, I used data from the Fall 2025 semester only. A polynomial regression model with a degree of 4 was applied to capture the non-linear pattern of academic workload over time, which increases at the beginning of the semester, decreases in the middle, and rises again toward the end.I chose polynomial regression because as the limited dataset size could lead to overfitting and unstable predictions when compex models are used. The same regression-based approach was applied to model weekly movie-watching behavior in spring term.

<img width="979" height="470" alt="2cbb1134-913f-4b8c-ae50-9aa1f1722dfb" src="https://github.com/user-attachments/assets/efbc152f-a3e4-43bb-afa9-f35d2196f0e4" />


## Limitations and Future Work 
This project was limited to my own academic workload and movie watching history covering only two semesters which resulted in a small dataset. Moreover, the machine learning models isn't able capture the relationship.In future work, using data from multiple semesters ,when I add new data, could help further develop and improve this analysis.


