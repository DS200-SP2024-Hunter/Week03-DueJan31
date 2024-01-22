# Lab Assignment for Week 03
## Simulation-based distribution of the sample median
## Due on [Canvas](https://psu.instructure.com/courses/2306358/assignments/15933445) on Wed., Jan. 31 at 11:59pm

The main objective of today's lab is to duplicate some of the sample mean analysis you did on the [recent homework](https://psu.instructure.com/courses/2306358/quizzes/5001947), but for the sample median.

**A quick note on the big picture here:**  Analyzing the distribution of the sample median is way too difficult to be part of a typical introductory statistics course.  But because we can carry out part of this analysis using simulation, it's a great thing to do in a data science course. 

The code will be based on Sections 10.2 and 10.3 of the textbook, which deals with a 13,825-row dataset of United Airlines flights.  Thus, I recommend starting with the code (i.e., the Jupyter Notebook) from Section 10.2 or 10.3, then copy-and-pasting code from the other section as needed.  To do this, follow steps 1 through 6 from [Lab 01](https://github.com/DS200-SP2024-Hunter/Week01-DueJan17) but in step 6 scroll to, then select, the notebook labeled "chapters/10/2/Sampling_from_a_Population.ipynb" or "chapters/10/3/Empirical_Distribution_of_a_Statistic.ipynb".

To successfully run either of the notebooks above, you'll need to change the value of the `path_data` object in the first code block; otherwise, the dataset will not be found by your colab environment.  You can do this by replacing the existing line defining `path_data` by this line:  `path_data = 'https://github.com/data-8/textbook/tree/main/assets/data'`

Remember that you can execute the code inside any python-code window by typing "shift-Return" inside that window.   Additionally, you can add a box for code or a box for text using the "+ Code" and "+ Text" buttons near the top left.  If you use Section 10.2 or 10.3 as the basis for your work, please try to delete irrelevant text and code boxes before you turn in your lab.

**Objective:**  Download a dataset with more than 350K rows on the bike share service in the Bay Area in California.  Using the duration of each trip in seconds, consider these 350K measurements to represent a large population.  Analyze the behavior of sample medians for samples of size 100 and 400 by simulating 5000 samples for both sample sizes.  _This dataset is analyzed in [Section 8.5 of the textbook](https://inferentialthinking.com/chapters/08/5/Bike_Sharing_in_the_Bay_Area.html), in case you want to learn more about it._

**Your assignment is as follows.** Please insert text boxes as appropriate, which should accompany all relevant code and output, to answer the questions below:

1. Download the dataset using the Table.read_table command from Section 10.2.  The dataset is called `trip.csv` and it may be accessed via `path_data + 'trip.csv'` just like the United flights dataset.

2. Find the smallest and largest values of the 'Duration' column.

3. Produce a histogram of Duration. Please choose your histogram bin boundaries so that you get a reasonable sense of the shape of the dataset, even if you have to exclude some of the very large values. Be sure to change the unit to "second" so that the axis labels are correct in your plot.

4. What fraction of the Duration values did you exclude from your histogram?  Give a precise numerical answer.

5. Find the mean and median value of Duration.  For the median, you'll need to use some code from Section 10.3, and the mean involves an obvious change.  This dataset has the property that the mean is larger than the median because the shape of the historgram has a long tail in the positive direction (a long tail in a distribution tends to affect the mean but not the median).    

6. Simulate 5000 samples of size 100 from the  Duration column.  Create a histogram of the 5000 sample medians that result.  Repeat this process using samples of size 400.

7. Comment on the distributions of the sample median.  What can you say about the shape of the distributions, the centers of the distributions (in relation to the population quantity of interest, the median), and the comparison between the "widths" of the two histograms?

When you've completed this, you should select "Print" from the File menu, then somehow save to pdf using this option.  The pdf file that you create in this way is the file that you should upload to Canvas for grading.  Recall that sometimes the right side of the notebooks are chopped off by this print procedure, but we have found that if you can select the "A3" paper size from the advanced options, this seems to solve the problem.

