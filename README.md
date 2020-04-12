# Intro-to-Trees
title: "Introduction to trees"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
# Plotting a Histogram
Frist we will plot a histogram for the Height of the trees.It is evident that the majority of the trees have a height of 79 feet.
```{r }
hist(trees$Height,20, col= "red")
```
# Plotting a Box plot
We can now plot a Box plot,whichwill show the variation amoungst our variables.
```{r }
boxplot(trees$Height,main= "Box plot", col = "green" )
```
We can see from the box plot below that the average Height value of the trees is around 76.
```{r }
boxplot(trees$Girth,main= "Box plot", col = "green" )
```
We can see from the box plot below that the average Girth value of the trees is around 13.
#Plotting a scatter plot
```{r }
plot(x=trees$Height, y=trees$Girth, main = "trees data Scatter plot", xlab="Height", ylab="Girth", col="green")
lin.mod = lm(trees$Girth~trees$Height)
pr.lm = predict(lin.mod)#Add line of best fit
lines(pr.lm~trees$Height, col="blue", lwd=0.7)
abline(mod <- lm(trees$Girth~trees$Height))
coef(mod)#calculate slope
```
