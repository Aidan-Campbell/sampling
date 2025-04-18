# Assignment: Questionnaire Design and Sample Evaluation

## Requirements

The goal of this assignment is to practice developing and evaluating sampling materials.

### Part A - Survey Design:

Select one of the scenarios below and design a survey to meet the need(s) outlined in the prompt.

1.	In two to three sentences, describe the purpose of your survey
2.	Describe your target population, sampling frame, sampling units, and overall sampling strategy.
3.	Write a 5-10 question survey to address your chosen scenario below.

##### Scenarios
1.	You work in the Human Resources Department at a large tech company. Over the past few months, the company has been experiencing a high turnover rate across many of its departments, specifically within the entry- and lower-level positions. The company wishes to understand why this turnover is happening, and what changes need to occur to improve employee satisfaction.
2.	You work for a Canadian national political party during a federal election. Throughout the campaign period, your party has seen relatively high approval ratings, but an opposing party is also polling favorably and may still have a chance to win the election. You are one month away from the election and you want to understand what voters want from your party and its leader in order to maintain your lead and eventually win the election.
3.	You are a student researcher in the sociology department at the University of Toronto. You are working on a research project that concerns the relationship between music taste and age. This involves both comparisons between different people of different ages and comparisons of the same individual at different ages during their lifetime. You wish to understand to what extent age influences music taste, specifically as it relates to perceptions of popular music. Your results will be written into an academic paper that you hope to publish.

### Part B - Survey Evaluation:

For the **Canadian General Social Survey on Giving, Volunteering, and Participating, 2018 (cycle 33)**, conducted by Statistics Canada find any and all available documentation for the data gathered and identify and describe the survey features indicated below.

1. Sample type
2. Sample size
3. Target population
4. Sampling frame
5. Survey mode(s) 
6. Timeline
7. Response rate
8. Weights
9. Data processing
10. Cleaning, imputation, etc
11. Sources of error
12. Limitations, known biases, etc
13. Link to documentation and any additional sources used


# Your Changes

## Part A - Survey Design: 

The number of your chosen topic: `#1`

Describe the purpose of your survey:
```
write your answer here... The purpose of the survey is to investigate and identify potential causes (i.e., initial observational evidence) for employee turnover and assess employee perceptions of how the company can change to improve employee wellbeing (and, thus, overall retention). The survey will include several brief face-valid measures to estimate constructs that are intended to capture wellbeing (e.g., burnout, happiness, meaning), and perceptions of company performace (e.g., workload, upskilling, upward mobility).
```

Describe your target population, sampling frame, sampling units, and observational units:
```
write your answer here... The target population will be all current and former entry- and lower-level employees of the company. The sampling frame will be records of current and past employees from the previous 10 years (for the sake of maintaining some level of recency - but pending history/size of the company, maybe 5 years). Sampling units would be each employee ID (current/former; and their respective contact information). Observational units would be each employee's survey responses.

To justify the use of a census format (hence the each former and current employee ID), as opposed to clustering or stratifying, I likely have data for how employees are organized (e.g., their departments) and am also in my make-believe world. So, I would ideally get as big of a sample as possible and run a hierarchical model to look at employee clustering (i.e., if there are meaningful trends by department).

It was hard to know the best approach without more context about number of employees that left vs. how many are currently with, how the company is organized (e.g., locations, departments and their size). I could imagine something like stratified sampling if the departments are relatively unequal in size so that I ensure each department is represented (e.g., sample 20 past/present employees per department). Perhaps organize strata by location and department if it's a massive company (e.g., ensuring different nations are represented as well). HLMs would obviously still make sense here as well.
```

Your 5-10 question survey:
```
Note 1: I'd have two versions of each question, coded to change based on whether employee is current or former so that items are properly worded (either via an initial screener or just separate survey paths pending ID). For ske of ease, I'll just word them for current employees.

Note 2: I'm aware of the potential for acquiescence bias here as all of them are positively-keyed. I might consider switching out some of the lower items (i.e., upskilling, mobility, and valued) for a negatively-keyed item or two so that I could make a latent bias variable in the assumed analysis of this.

1. write your question here... Burnout: "Overall, I feel emotionally exhausted with work" (1- Strongly disagree to 7 - Strongly agree)
2. write your question here... Happiness: "Overall, I feel happy with my worklife" (1- Strongly disagree to 7 - Strongly agree)
3. write your question here... Meaning: "Overall, I feel a significant sense of purpose in my work" (1- Strongly disagree to 7 - Strongly agree)
4. write your question here... Job satisfaction: "Overall, I feel satisfied with my job" (1- Strongly disagree to 7 - Strongly agree)
5. write your question here... Workload: "Overall, I feel the company maintains a fair workload for me" (1- Strongly disagree to 7 - Strongly agree)
6. write your question here... (optional) Upskilling (wording is meh): "Overall, I feel the company provides enough opportunities for me to increase my skills and abilities that will help my career" (1- Strongly disagree to 7 - Strongly agree)
7. write your question here... (optional) Upward mobility: "Overall, I feel the company provides enough opportunities for me to move upwards (i.e., in terms of position, pay) in my career" (1- Strongly disagree to 7 - Strongly agree)
8. write your question here... (optional) Valued: "Overall, I feel that I am a valued part of the company" (1- Strongly disagree to 7 - Strongly agree)

Below are some more "wonky" questions I feel worth pursuing
9. write your question here... (optional) Intentions to stay (for current employees only): "Overall, I feel confident that I will stay at this company for the forseeable future" (1- Strongly disagree to 7 - Strongly agree)
10. write your question here... (optional) Area for improvement (free-response): Below are 3 boxes listed from 1, 2, and 3. In each box, please list, in a few words, areas which you believe the company could improve the most (e.g., employee benefits, pay, opportunities for promotions, workload, etc.). Please list them in order of importance (i.e., 1 - Most important to 3 - Less important). You do not need to fill out each box if you are unable to think of 3.   
```

## Part B - Survey Evaluation:

Identify and describe survey features:

```
write your answer here
1. Sample type Stratified probability sample with rejection sampling (from googling, rejection sampling is a markov chain monte carlo algorithm - I'm not totally sure, but looks interesting)
2. Sample size They anticipated 24,000 responses of 50,000 sampled households (1 person chosen per houehold)
3. Target population All non-institutionalized people 15 years and older living in private households across the 10 provinces.
4. Sampling frame: Phone numbers from census and "various administrative sources" along with Stat Can's dwelling frame.
5. Survey mode(s): Electronic questionnaire or phone-assisted computer questionnaire. 
6. Timeline 2004 to 2018 (though some version of this survey existed in 1997, and then again in 2000). For this specific cycle, it was just the year 2018 from Septembr 4th to December 28th.
7. Response rate 41.9%
8. Weights Estimation weights (WGHT_PER) and bootstrapping weights. For estimation weights, a given person in the sample is presumed to "represent" X amount of people from the total population. Becuse they used rejection samplng, and over-represent vounteers, they weighted non-volunteers who weren't rejected by multiplying their weighting by a "factor". They also weighted the income distribution to match the 2017 CIS distribution by province.
9. Data processing They linked data to personal and household tax records, household information, along with personal and household persons' information. They reference something called SSPE - which seem to be a collection of processing tools used by Stats Canada in a lot of their surveys. From what I understand, it's a standardized process for error detection - afterwhich edits to detected errors can be made in their CATI system.
10. Cleaning, imputation, etc It seems like they used nearest-neighbor matching most of the time but when that failed, they used mean imputation.
11. Sources of error: General sampling error (which they used bootstrpping to estimate esample variability) and non-sampling error (i.e., coverage error and non-response bias). They were sampling via phone numbers - so households without phones would be excluded along with houses that have phones not covered by the frame used. Of course, with non-response bias - people are not required to answer, and this likely captures a certain "type" of person. The systematic exclusion of this "type" likely biases the sample.
12. Limitations, known biases, etc I feel much of these get covered in the sources of error (in terms of limitations), but other response biases resulting from self-report are of course pron to socially desirable responding, careless responding, or limitations of memory. It seems like rejection sampling is used to over-represent thoe tht volunteer, so presumably this is prone to some biasing. Additionally, they did not cover the 3 territories, though the populations there are small, they likely meaningfully differ.
13. Link to documentation and any additional sources used
https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&Id=143876#a1 and
https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&amp;SDDS=4430
```

## Rubric

-	All required components are present and complete **Complete / Incomplete**
-	Choice of sampling strategy for Part A is justified and related to survey purpose **Complete / Incomplete**
-	Information for Part B is complete and correct **Complete / Incomplete**

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 18/04/2025`
* The branch name for your repo should be: `assignment-2`
* What to submit for this assignment:
    * This markdown file (a2_survey_design_and_evaluation.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-2`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
