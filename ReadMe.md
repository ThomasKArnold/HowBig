

# How Big Does Your Big Data Need To Be?

Thomas Arnold, PhD
arnoldtk@mail.uc.edu
June 27, 2021

One of the tenets of modern data science is that BIG DATA is important. The question is, how BIG does your BIG DATA need to be? The following analyses try to answer this question.

The proponents of big data propose that five Vs that are important in defining big data.  These Vs are volume, velocity, variety, veracity and value. I have not seen a lot of research that explores the connection between these five V concepts.  I was able to analyze four of the five Vs. The only V that is not involved in these calculations is velocity.

Three sets of analyses are provided to explore the connection between the 4 Vs. The first set of analyses indicate how increasing volume affects value. It will be demonstrated that increases in volume tend to have diminishing returns. The second set of analyses look at how veracity affects value. Increases in veracity also have diminishing returns. The third set of analyses show that variety is one of the more important factors in producing value because increases in variety are linearly associated with increases in value.

The analyses indicate that reaching the maximum value possible, which is a 100% prediction accuracy with R Squared = 1.000, can take some really BIG DATA if you don't have enough variety in your data. When the veracity is r=.05, it can take a volume of up to 90,000 variables to reach the maximum possible value. The reasons for this problem of diminishing returns for volume and veracity are discussed.

I am starting with the results of a three way analysis of volume, veracity, and value to highlight the problem.  One can get pretty good value with relatively small volume in the range of a few hundred variables or when one has high veracity to begin with.  However, at some point, the plot flattens out and one needs really BIG DATA to get much additional value.   

![r vs R Squared](https://github.com/ThomasKArnold/HowBig/blob/main/VolumeVeracityValue.png) 

I go on to explore the reasons for this phenomenon.  This is my first attempt at publishing to GitHub and I appreciate any comments.  Thanks in advance!

> Written with [StackEdit](https://stackedit.io/).
