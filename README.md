Analyze Death Age Difference of Right Handers with Left Handers.
Death age difference of right-handers and left-handers is an intriguing topic that has been studied by researchers for many years. Some studies have found that left-handers tend to die younger than 
right-handers, while others have found no significant difference.

There are a number of possible explanations for this observed difference in death age. One possibility is that left-handers are more likely to engage in risky behaviors, such as smoking and drinking,
which can lead to premature death. Another possibility is that left-handers are more likely to be exposed to environmental toxins, such as lead and pesticides, which can also shorten lifespan.

Finally, it is also possible that there is a biological difference between left-handers and right-handers that makes left-handers more susceptible to certain diseases, such as heart disease and
Alzheimer’s disease.

More research is needed to determine the exact cause of the observed difference in death age between right-handers and left-handers. However, the findings of existing studies suggest that it is a
complex issue with multiple contributing factors.

Significance of the topic The study of death age difference between right-handers and left-handers is significant for a number of reasons. First, it can help us to better understand the factors that
contribute to premature death. This knowledge can then be used to develop interventions to prevent premature death in both right-handers and left-handers.

Second, the study of death age difference between right-handers and left-handers can also help us to learn more about the biology of handedness. By understanding the biological differences between 
left-handers and right-handers, we may be able to develop new treatments for diseases that are more common in one group than the other.

Finally, the study of death age difference between right-handers and left-handers can also help to raise awareness of the unique challenges faced by left-handers in society. By understanding the 
health risks associated with left-handedness, we can work to create a more inclusive society that supports all people, regardless of their handedness.

The project is solved using the six-phases of data analysis: — Ask, Prepare, Process, Analyze, Share and Act.

Solution

Ask

The ask phase is the start of the data analysis cycle, it involves clearly defining the scope of the project, the problem to be solved, and identifying stakeholders and stakeholder’s 
expectations by asking SMART (Specific, Measurable, Action-oriented, Relevant, Time-bound) questions.

The following questions may guide us to our analysis: -

Load the handedness data from the National Geographic survey and create a scatter plot of “Left-handed Rate” vs. “Age”. Add two new columns, one for birth year and one for mean left-handedness,
then plot the mean as a function of birth year. Create a function that will return P(LH | A) for particular ages of death in a given study year. Load death distribution data for the United States and plot it. Create a function called P_lh() which calculates the overall probability of left-handedness in the population for a given study year. Write a function to calculate P_A_given_lh(). Write a function to calculate P_A_given_rh(). Plot the probability of being a certain age at death given that you’re left- or right-handed for a range of ages. Find the mean age at death for left-handers and right-handers. Redo the calculation from Task 8, setting the study_year parameter to 2018. Prepare

This includes identifying the source of the information that will be utilized for the analysis, guaranteeing that the information source is dependable, unique, thorough, current and referred to,
demonstrating the knowledge, ensuring that the information is liberated from any bias in the assortment of the information and, regarding each part of data ethics while dealing with the information.

This notebook uses two datasets: death distribution data for the United States from the year 1999 (source website here) and rates of left-handedness digitized from a figure in this 1992 paper by 
Gilbert and Wysocki.

The data’s credibility and integrity can be assessed in the framework of the ROCCC.

Reliability: The data is reliable due to its sample size (approx. 7 million people). Originality: The datasets are original. They were collected by CDC. Comprehensiveness: The data is 
comprehensive due to data having features like nationality, handedness, age, sex and race. Current: The data was collected during the 1986. Hence it is outdated. Cited: It was cited by CDC 
and 1992 paper by Gilbert and Wysocki. Process

This involves all the steps taken to clean the data, making sure the data has integrity (the data is accurate, complete, consistent and trustworthy) before analyzing it, aligning the data to 
the business objective and also carrying out data verification. We must sure that the process involves checking of misspellings, inconsistent capitalizations and typos, checking for duplicate 
entries and blank cells and checking for consistent data format across each column.

Since the data is in the form of pdf formats, which already consists of clean quality data, there is not much data cleaning process involved. The technical skill used in this project is Python 
programming language. The IDE used here is Jupyter Notebook. Python libraries such as pandas, NumPy and matplotlib.pyplot will be used to analyze the dataset to solve the given tasks.

Analyze and Share

Load the handedness data from the National Geographic survey and create a scatter plot of the “Left-handed Rate” vs. “Age”. In this notebook, we will explore this phenomenon using age distribution 
data to see if we can reproduce a difference in average age at death purely from the changing rates of left-handedness over time, refuting the claim of early death for left-handers. This notebook uses
pandas and Bayesian statistics to analyze the probability of being a certain age at death given that you are reported as left-handed or right-handed.

A National Geographic survey in 1986 resulted in over a million responses that included age, sex, and hand preference for throwing and writing. Researchers Avery Gilbert and Charles Wysocki 
analyzed this data and noticed that rates of left-handedness were around 13% for people younger than 40 but decreased with age to about 5% by the age of 80. They concluded based on analysis of a 
subgroup of people who throw left-handed but write right-handed that this age-dependence was primarily due to changing social acceptability of left-handedness. This means that the rates aren’t a 
factor of age specifically but rather of the year you were born, and if the same study was done today, we should expect a shifted version of the same distribution as a function of age. Ultimately, 
we’ll see what effect this changing rate has on the apparent mean age of death of left-handed people, but let’s start by plotting the rates of left-handedness as a function of age.
