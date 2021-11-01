# myTuwaiqDSProj
# Abstract
This work is proposed to investigate the possible association between programming languages and open-source software development in a large-scale setting using data science tools and techniques. It is to examine whether there is evidence that indicates a relationship between language choice and OSS projects. A comparison is to be made between projects written in different languages based on mining project's repository data on Github. Project attributes such as the main language, number of languages, project size, number of commits, number of contributors, number and type of bugs, and project duration are to be used for this comparison to inspect and understand the relationship between language design and OSS projects. The methodology is based on mining software repositories, and the results obtained from the analysis of a sample with 5,350 projects out of a total of 15,000 projects where a main language can be identified.

# Motivation/Need
Two studies have investigated the impact of programming language design on code quality. The results reported in the first work were based on an observational study with a corpus of 729 GitHub projects written in 17 programming languages. They found that languages significantly impact code quality [1]. The study was replicated in 2019 [2], they first reproduced the findings with the same 729 projects following the same methodology and analysis resulted in a partially successful replication. After that, they re-analysed the included projects following different methodology for processing and analysis than the original one. As a result, a smaller number of projects were included (423 projects) and most of the claims did not hold. In addition, for the cases where the claims did hold, the relationship between programming language and defects were found to be exceedingly small in effect size.
The two datasets that have been used in the previous works are very small to obtain conclusive findings. Thus, in this work I’m going to revisit their findings and investigate the association between language and code quality in terms of number and type of bugs, along with other projects attributes in a larger-scale setting by taking advantage of data science tools and techniques.


# Questions
1. 	Is there an association between language choice and open-source project attributes?
* 	What is the significance and magnitude of such an association, if any?
* 	Would findings hold If we controlled for differences in project size and type?
Project attributes: code quality in terms of number and type of bugs, number of languages, number of commits, number of contributors,  project size, duration, project type.
2. 	What are the types of the included projects? (analyzing projects description to get their type, NLP)
3.	What are the bugs types? (analyzing bugs description to get their type, NLP)


# Preliminary Design
Group projects based on their main language into 3 different binary classifications (static vs dynamic, memory managed vs unmanaged, and strongly typed vs weakly typed languages).
For each classification investigate the following:
1.	The association/relationship/correlation between language design and {project attribute}
2.	The significance and magnitude of such association, if any.
* Method: Regression analysis and hypothesis test.
3.	Identify projects type.
4.	Identify bugs type.
*	Method: topic modeling using the Latent Dirichlet Allocation (LDA).
Project attributes: code quality in terms of number and type of bugs, number of languages, number of commits, number of contributors,  project size, project duration, project type.
5. Validate the findings. Still not sure. 


# Data Description
A sample of 5,350 projects from a total of 15,000 projects on Github. The selected projects have the following characteristics:
*	The project should have at least 500 stars.
*	The project should have a main language, which makes up 95% of its total code.
*	The main language should be a high-level, and general-purpose one.

The collected data include a project description, number of languages, number of commits, number of contributors,  project size, project duration, project type. We still need to pull bugs description and number, however, the other data has been already pulled and stored.

## Dataset snippet
<a href="https://ibb.co/nmLpst2"><img src="https://i.ibb.co/zx4dhDc/Capture.jpg" alt="Capture" border="0"></a><br /><a target='_blank' href='https://the-crosswordsolver.com/u-s-n-rank-below-capt-4-letters'></a><br />
 
# Tools
*	Data manipulation and analysis: Numpy and Pandas for numeric data, NLP using LDA for topic modeling. 
*	Data modeling: Scikit-learn 
*	Plotting: Matplotlib and Seaborn
*	Visualization: Tableau for interactive visualizations


# References
[1] Ray, B., Posnett, D., Filkov, V., & Devanbu, P. (2014, November). A large-scale study of programming languages and code quality in Github. In Proceedings of the 22nd ACM SIGSOFT International Symposium on Foundations of Software Engineering (pp. 155-165).

[2] Berger, E. D., Hollenbeck, C., Maj, P., Vitek, O., & Vitek, J. (2019). On the impact of programming languages on code quality: a reproduction study. ACM Transactions on Programming Languages and Systems (TOPLAS), 41(4), 1-24.
