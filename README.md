# Reproducible research: version control and R

## Answers

### Questions 1 - 3

Link to logistic growth repo:

<https://github.com/dusty-saxophone/logistic_growth>

### Question 4

#### 4.1

![](https://github.com/dusty-saxophone/reproducible-research_homework/blob/main/Graphs/random_walks.png)

The code generates two 2D plots representing two different random walks. The route taken is represented by a line traveling through a two 2D space of x and y coordinates. The route semms to start at point (0,0) and comprises of 500 different steps, each 0.25 units long. The timing of steps taken is represented by a colour gradient; earlier steps in the route are darker than steps later in the route.

#### 4.2 - Random seeds

Computers are incapable of producing truly random numbers de novo. There are some "true" random number generators which rely on measures of randomness from highly stochastic environmental conditions like radioactive decay. However, most random number generators are pseudo-random or deterministic. These are numbers generated by computer algorithms to appear impossible to predict but in reality have an underlying pattern.

A random seed is a value (in number or vector form) which is used to initialise a pseudo-random number generator. The seed value acts as the intial state variable for the algorithm and undergoes a randomness function set out by the algorithm to generate a second number. This new number then becomes the state variable and the process repeats. As these algorithms are deterministic, if the same seed (starting point) is used, the same sequence of "random" numbers is generated.

#### 4.3 - Brownian motion

<p align="center">

![](https://github.com/dusty-saxophone/reproducible-research_homework/blob/main/commit_comparison.png)

<p>

### Question 5

#### 5.1 - Data table

Columns = 13

Rows = 33

#### 5.2 - Transformation

Transformations:

1.  Log transformation of virion volume (nm<sup>3</sup>)

2.  Log transformation of genome length (kb)

Transformed data:

<p align="center">

![](https://github.com/dusty-saxophone/reproducible-research_homework/blob/main/question-5-data/transformed_data.png)

<p>

#### 5.3 - Linear model

``` math
\begin{equation}
V = \alpha L^{\beta}
\end{equation}
```

## Instructions

The homework for this Computer skills practical is divided into 5 questions for a total of 100 points. First, fork this repo and make sure your fork is made **Public** for marking. Answers should be added to the \# INSERT ANSWERS HERE \# section above in the **README.md** file of your forked repository.

Questions 1, 2 and 3 should be answered in the **README.md** file of the `logistic_growth` repo that you forked during the practical. To answer those questions here, simply include a link to your logistic_growth repo.

**Submission**: Please submit a single **PDF** file with your candidate number (and no other identifying information), and a link to your fork of the `reproducible-research_homework` repo with the completed answers (also make sure that your username has been anonymised). All answers should be on the `main` branch.

## Assignment questions

1)  (**10 points**) Annotate the **README.md** file in your `logistic_growth` repo with more detailed information about the analysis. Add a section on the results and include the estimates for $N_0$, $r$ and $K$ (mention which \*.csv file you used).

2)  (**10 points**) Use your estimates of $N_0$ and $r$ to calculate the population size at $t$ = 4980 min, assuming that the population grows exponentially. How does it compare to the population size predicted under logistic growth?

3)  (**20 points**) Add an R script to your repository that makes a graph comparing the exponential and logistic growth curves (using the same parameter estimates you found). Upload this graph to your repo and include it in the **README.md** file so it can be viewed in the repo homepage.

4)  (**30 points**) Sometimes we are interested in modelling a process that involves randomness. A good example is Brownian motion. We will explore how to simulate a random process in a way that it is reproducible:

    a)  A script for simulating a random_walk is provided in the `question-4-code` folder of this repo. Execute the code to produce the paths of two random walks. What do you observe? (10 points)\
    b)  Investigate the term **random seeds**. What is a random seed and how does it work? (5 points)\
    c)  Edit the script to make a reproducible simulation of Brownian motion. Commit the file and push it to your forked `reproducible-research_homework` repo. (10 points)\
    d)  Go to your commit history and click on the latest commit. Show the edit you made to the code in the comparison view (add this image to the **README.md** of the fork). (5 points)

5)  (**30 points**) In 2014, Cui, Schlub and Holmes published an article in the *Journal of Virology* (doi: <https://doi.org/10.1128/jvi.00362-14>) showing that the size of viral particles, more specifically their volume, could be predicted from their genome size (length). They found that this relationship can be modelled using an allometric equation of the form $`V = \alpha L^{\beta}`$, where $`V`$ is the virion volume in nm<sup>3</sup> and $`L`$ is the genome length in nucleotides.

    a)  Import the data for double-stranded DNA (dsDNA) viruses taken from the Supplementary Materials of the original paper into Posit Cloud (the csv file is in the `question-5-data` folder). How many rows and columns does the table have? (3 points)\
    b)  What transformation can you use to fit a linear model to the data? Apply the transformation. (3 points)\
    c)  Find the exponent ($\beta$) and scaling factor ($\alpha$) of the allometric law for dsDNA viruses and write the p-values from the model you obtained, are they statistically significant? Compare the values you found to those shown in **Table 2** of the paper, did you find the same values? (10 points)\
    d)  Write the code to reproduce the figure shown below. (10 points)

<p align="center">

<img src="https://github.com/josegabrielnb/reproducible-research_homework/blob/main/question-5-data/allometric_scaling.png" width="600" height="500"/>

</p>

e)  What is the estimated volume of a 300 kb dsDNA virus? (4 points)
