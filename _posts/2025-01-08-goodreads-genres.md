---
title: "Goodreads Genres"
date: 2025-01-08
image: "/assets/images/goodreads/thumbnail.svg"
---
I was interested in whether particular book genres are more highly rated by readers than others. Based on my experience on the Goodreads website, I was expecting to see very high ratings for fantasy and young adult books, which are quite popular. I had a lot of fun making this and learning how to webscrape with the rvest package (Goodreads' API is no longer available). I took data only from the 50 most shelved books per the selected genres, so this may have influenced the results.

<img src="/assets/images/goodreads/ridgeplot.svg" style="height:500px;width:620px;margin:auto;" />

I chose to separate high fantasy and "romantasy" somewhat arbitrarily based on my own opinion that they attract quite different followings. However, there may be quite a bit of overlap between the two.

I performed a Welch's one-way ANOVA and Games-Howell post-hoc test to determine whether significant differences existed between the genres' average ratings (the assumption of homogeneity of variances was not met for a regular ANOVA).

High fantasy was more highly rated than all other genres (except romantasy). Romantasy was more highly rated than everything except for science fiction and young adult (and high fantasy). Science fiction was more highly rated than the classics.
