How Big Does Your Big Data Need To Be?

Thomas Arnold, PhD
arnoldtk@mail.uc.edu
June 11, 2021

The purpose of these analyses was to determine how many variables with r(x,y) are needed to achieve an R Squared = 1.000. These calculations initially began in SPSS and I am transitioning to Python as a learning experience. Python also provides the ability to post to Github.

I used ordinary least squares (OLS) regression because all of the variables were random normal. No assumptions of the OLS regression model were violated.

I set up the regression models using randomly correlated variables. These correlated variables (r(x,y) are created using the following formula.

x(r) = Y * r + x * np.sqrt(1-r**2)

Where 	x(r) = The correlated x variable 
	Y = A random variable 
	r = The desired correlation 
	x = A random variable

The analyses turned out to be informative. One finding was that inter-correlation has big effects on model accuracy.

The first SPSS example I used for building correlated variables had a factor analysis included. I found that using the factor analyses, and creating factor variables from the correlated variables, I could create a smaller subset of correlated variables with no inter-correlation. When I did this, I found that the R Squared = 1.000 was easy to achieve with only a few variables. This model is replicated in an easier fashion using the Choloesky Decomposition. Factor analyses could be used to produce the same results.

The second set of analyses involved creating varying numbers of variables that had varying r values. In this case, inter-correlation occurred naturally. The r(x,y) values ranged from .05 to .999. These analyses indicate that the R Squared increases quickly at first as more variables are added to the OLS regression model and then the gains from adding more variables start to drop rapidly.

For example, it would take 90,000 variables with r(x,y) to achieve an R Squared of 1.000. The (r, N, R Squared) plot I generated so far is included. I think that I may have to redo some calculations since it seems that the R Squared values from SPSS are higher than the R Squared values I get from Python.

I could also put this in an automated loop to get the values. Note however, that trying to run these models with over 50,000 variables is extremely RAM intensive and time consuming. I had to bump up my RAM to 128GB and it still took about a week for some of these calculations to finish when the variable count got up to 100,000.

I probably need to add some sections to look at what the inter-correlation levels are for each r(x,y). I also don't like the look of the plot. Excel has a smoothing function that reduces the granularity.
