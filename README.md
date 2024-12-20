# Reproducible research: version control and R

1) Answered in https://github.com/1075515/logistic_growth/tree/main
2) Answered in https://github.com/1075515/logistic_growth/tree/main
3) Answered in https://github.com/1075515/logistic_growth/tree/main
4) See file: https://github.com/1075515/reproducible-research_homework/blob/main/question-4-code/random_walk.R

   a) This script produces unpredictable, randomised walks in two side-by-side line graphs consisting of zig-zag lines. Although the same parameters are used for each of the graphs, the outcomes differ, and running the code multiple times leads to different patterns each time. The lines always start at the origin (0,0), with the darkest blue colour indicating the start of the path (when time=1), which becomes lighter with each step (as time goes to 500). The randomness in the pattern comes from the angle generated by the code rather than the distance. The distance between each zig-zag is always 1 step of 0.25 arbitrary units, making up 500 steps in total.

   b) Random seeds ensure the reproducibility of a sequence of random numbers generated by a pseudorandom number generator. This means the same output will be reproduced when the code is rerun, for example, by other users. This is most commonly used for code-based simulations and random samples. 
 
   For example, the set.seed() function in R guarantees that the same random values are produced each time any code is run, which involves random number generation. Any chosen number (the seed) is inserted into the function, and this seed-fixing is crucial. Without setting a seed, the random number generator will produce values which are unlikely to produce the same output after rerunning the code. After using set.seed() with the same seed value, the same values will be outputted each time, making the results reproducible. 


   c) See: https://github.com/1075515/reproducible-research_homework/blob/main/question-4-code/random_walk.R

   d) 
   ![code_edit](https://github.com/user-attachments/assets/4f456e83-90fe-457c-a1e7-1cc46f336861)


5) See file: https://github.com/1075515/reproducible-research_homework/blob/main/question-5-code.R

   a) The table has 33 rows and 13 columns. 

   b) A logarithmic transformation should be used to fit a linear model to the data _(see code)_. 

   c) For dsDNA viruses, the allometric exponent (β) is 1.5152 (p=2.28e-10) and the scaling factor (α) is 1181.807 (p=6.44e-10). The p values are <0.01 so both are statistically significant. This indicates that there is a statistically significant relationship between virion volume and genome length. In Table 2 of the paper, the allometric exponent (β) was 1.52 and the scaling factor (α) was 1182. When rounded, the values I found (1.5152 for β and 1181.807 for α) are consistent with those found in Table 2. 

   d) See: https://github.com/1075515/reproducible-research_homework/blob/main/question-5-code.R
   
   e) The estimated volume of a 300kb dsDNA virus is 6,697,006 nm^3 (_See question-5-code.R for workings_)


## Instructions

The homework for this Computer skills practical is divided into 5 questions for a total of 100 points. First, fork this repo and make sure your fork is made **Public** for marking. Answers should be added to the # INSERT ANSWERS HERE # section above in the **README.md** file of your forked repository.

Questions 1, 2 and 3 should be answered in the **README.md** file of the `logistic_growth` repo that you forked during the practical. To answer those questions here, simply include a link to your logistic_growth repo.

**Submission**: Please submit a single **PDF** file with your candidate number (and no other identifying information), and a link to your fork of the `reproducible-research_homework` repo with the completed answers (also make sure that your username has been anonymised). All answers should be on the `main` branch.

## Assignment questions 

1) (**10 points**) Annotate the **README.md** file in your `logistic_growth` repo with more detailed information about the analysis. Add a section on the results and include the estimates for $N_0$, $r$ and $K$ (mention which *.csv file you used).
   
2) (**10 points**) Use your estimates of $N_0$ and $r$ to calculate the population size at $t$ = 4980 min, assuming that the population grows exponentially. How does it compare to the population size predicted under logistic growth? 

3) (**20 points**) Add an R script to your repository that makes a graph comparing the exponential and logistic growth curves (using the same parameter estimates you found). Upload this graph to your repo and include it in the **README.md** file so it can be viewed in the repo homepage.
   
4) (**30 points**) Sometimes we are interested in modelling a process that involves randomness. A good example is Brownian motion. We will explore how to simulate a random process in a way that it is reproducible:

   a) A script for simulating a random_walk is provided in the `question-4-code` folder of this repo. Execute the code to produce the paths of two random walks. What do you observe? (10 points) \
   b) Investigate the term **random seeds**. What is a random seed and how does it work? (5 points) \
   c) Edit the script to make a reproducible simulation of Brownian motion. Commit the file and push it to your forked `reproducible-research_homework` repo. (10 points) \
   d) Go to your commit history and click on the latest commit. Show the edit you made to the code in the comparison view (add this image to the **README.md** of the fork). (5 points) 

5) (**30 points**) In 2014, Cui, Schlub and Holmes published an article in the *Journal of Virology* (doi: https://doi.org/10.1128/jvi.00362-14) showing that the size of viral particles, more specifically their volume, could be predicted from their genome size (length). They found that this relationship can be modelled using an allometric equation of the form **$`V = \alpha L^{\beta}`$**, where $`V`$ is the virion volume in nm<sup>3</sup> and $`L`$ is the genome length in nucleotides.

   a) Import the data for double-stranded DNA (dsDNA) viruses taken from the Supplementary Materials of the original paper into Posit Cloud (the csv file is in the `question-5-data` folder). How many rows and columns does the table have? (3 points)\
   b) What transformation can you use to fit a linear model to the data? Apply the transformation. (3 points) \
   c) Find the exponent ($\beta$) and scaling factor ($\alpha$) of the allometric law for dsDNA viruses and write the p-values from the model you obtained, are they statistically significant? Compare the values you found to those shown in **Table 2** of the paper, did you find the same values? (10 points) \
   d) Write the code to reproduce the figure shown below. (10 points) 

  <p align="center">
     <img src="https://github.com/josegabrielnb/reproducible-research_homework/blob/main/question-5-data/allometric_scaling.png" width="600" height="500">
  </p>

  e) What is the estimated volume of a 300 kb dsDNA virus? (4 points) 
