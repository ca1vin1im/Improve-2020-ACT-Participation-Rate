# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Improve 2020 ACT Participation Rate

### Background
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). 

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

### Datasets selected
- `act_2017.csv`: 2017 ACT Scores by State
- `act_2018.csv`: 2018 ACT Scores by State
- `act_2019.csv`: 2019 ACT Scores by State
- `sat_2017.csv`: 2017 SAT Scores by State
- `sat_2018.csv`: 2018 SAT Scores by State
- `sat_2019.csv`: 2019 SAT Scores by State


The 6 datasets above provides data on the participation rate of high school students in each state who took the ACT and/or SAT in 2017, 2018 and 2019, and with their average scores aggregated at state-level. They will be used to identify states where ACT/SAT participation rates have increased/decreased significantly over the years.

---

### Problem Statement
- Analyse trends in both the ACT and SAT participation rates to identify potential strategies for improving 2020 ACT participation rates and eventually reclaim its position as the nation’s most widely used college admission test. The rival College Board's SAT is more widely taken by graduating seniors since 2018 ([*source*](https://www.washingtonpost.com/education/2018/10/23/sat-reclaims-title-most-widely-used-college-admission-test/)). In the class of 2019, over 2.2 million students ([*source*](https://www.prnewswire.com/news-releases/over-2-2-million-students-in-class-of-2019-took-sat-largest-group-ever-300923736.html)) took the SAT as compared to over 1.78 million graduates ([*source*](https://www.act.org/content/dam/act/unsecured/documents/National-CCCR-2019.pdf)) who took the ACT.

---

### Data Dictionaries:

**For modified ACT dataset    (Filename: `modified_act_merged.csv`)**:

|Feature|Type|Description|
|---|---|---|
|state|*object*|States where the high school graduates who took the ACT reside in.|
|act_participation_rate_2017|*float*|Percentage (in 2 decimal places) of the state's high school graduates who took the ACT in 2017, e.g. 0.25 means 25%.|
|act_total_score_2017|*integer*|Composite (average of scores for English, Math, Reading, Science) score (1-36) of high school graduates by state in 2017.|
|act_participation_rate_2018|*float*|Percentage (in 2 decimal places) of the state's high school graduates who took the ACT in 2018, e.g. 0.25 means 25%.|
|act_total_score_2018|*integer*|Composite (average of scores for English, Math, Reading, Science) score (1-36) of high school graduates by state in 2018.|
|act_participation_rate_2019|*float*|Percentage (in 2 decimal places) of the state's high school graduates who took the ACT in 2019, e.g. 0.25 means 25%.|
|act_total_score_2019|*integer*|Composite (average of scores for English, Math, Reading, Science) score (1-36) of high school graduates by state in 2019.|
|act_delta_1718|*float*|Percentage change (in 2 decimal places) in state's participation rate from 2017 to 2018.|
|act_delta_1819|*float*|Percentage change (in 2 decimal places) in state's participation rate from 2018 to 2019.|


**For modified SAT dataset    (Filename: `modified_sat_merged.csv`)**:

|Feature|Type|Description|
|---|---|---|
|state|*object*|States where the high school graduates who took the SAT reside in.|
|sat_participation_rate_2017|*float*|Percentage (in 2 decimal places) of the state's high school graduates who took the SAT in 2017, e.g. 0.25 means 25%.|
|sat_total_score_2017|*integer*|Average Total (EBRW + Math) score (400-1,600) of high school graduates by state in 2017.|
|sat_participation_rate_2018|*float*|Percentage (in 2 decimal places) of the state's high school graduates who took the SAT in 2018, e.g. 0.25 means 25%.|
|sat_total_score_2018|*integer*|Average Total (EBRW + Math) score (400-1,600) of high school graduates by state in 2018.|
|sat_participation_rate_2019|*float*|Percentage (in 2 decimal places) of the state's high school graduates who took the SAT in 2019, e.g. 0.25 means 25%.|
|sat_total_score_2019|*integer*|Average Total (EBRW + Math) score (400-1,600) of high school graduates by state in 2019.|
|sat_delta_1718|*float*|Percentage change (in 2 decimal places) in state's participation rate from 2017 to 2018.|
|sat_delta_1819|*float*|Percentage change (in 2 decimal places) in state's participation rate from 2018 to 2019.|

---

### Selected Findings:
- Colorado state mandated SAT for all high school juniors effective 11Apr2017, resulting in drastic drop of its ACT participation rate to 30% and lower beyond 2017. [(source)](https://testive.com/colorado-sat-change-2017/)
- The College Board won a 3-year $14.3 million bid upon expiry of the ACT exam contract in 30Jun2016 to give its SAT exam to all public high school juniors in Illinois, resulting in drastic drop of Illinois' ACT participation rate to 43% and lower beyond 2017. [(source)](https://www.chicagotribune.com/news/ct-illinois-chooses-sat-met-20160211-story.html)
- Alaska's high school students no longer required by state law to take the SAT, ACT or WorkKeys test to get their diplomas as the law expired 30Jun2016. This resulted in a drastic drop of Alaska's ACT participation rate to 65% and lower for 2017 and 2018. Alaska's ACT participation rate increased slightly by 5% to 38% in 2019. [(source)](https://www.adn.com/alaska-news/education/2016/06/30/students-no-longer-need-national-tests-to-graduate/)
- More Florida students took the SAT in 2018 than ever before, pushed by free test sessions at their schools, resulting in drop of its ACT participation rate to 66% and lower beyond 2017. [(source)](https://www.orlandosentinel.com/news/education/os-ne-act-sat-florida-scores-20181024-story.html)
- Ohio state funds either the SAT or ACT test effective Apr2017, with 95% of districts picking the ACT which is $2.50 less expensive than the SAT per test. [(source)](https://www.cleveland.com/metro/2017/04/free_sat_or_act_exams_give_all.html)
- Nebraska State mandated state accountability testing at the high school level be completed via the ACT test effective spring 2017 to all public school third-year cohort students, except those identified as needing alternate assessment. [(source)](https://www.education.ne.gov/assessment/act/)
- Rhode Island adopted both the PSAT and SAT tests for high school students in 2017, mandating both tests as a graduation requirement in 2018 as part of the state’s federal education plan. [(source)](https://www.providencejournal.com/story/news/education/2018/10/25/with-sat-required-ri-sees-jump-in-participation-decline-in-scores/9450299007/)
- West Virginia chose The College Board's SAT as the new statewide standardized test for high school juniors effective spring 2018 because it provides valuable resources at a lower cost than ACT. The contract initially will be for one year, with the option of three 1-year renewals. Students may still use the ACT to qualify for the state's Promise Scholarship. [(source)](https://www.wvgazettemail.com/news/education/wv-chooses-sat-as-new-high-school-standardized-test-for-juniors/article_b60d2618-4943-56f6-b180-4b4442172ef8.html)
- Arizona allows for its 55 public schools to measure high school students’ proficiency in Arizona academic standards with the ACT or SAT effective 2019 instead of AzMERIT. 44 of these 55 schools chose ACT over SAT, citing reasons of lesser time needed to take the ACT (vs AzMERIT), greater student ownership, value and meaning. This probably led to the rise in ACT participation rate by 7% from 2018 in 2019. [(source)](https://azednews.com/why-some-schools-chose-the-act-or-sat-over-azmerit/)
- Further to what has been highlighted in Finding #12 above, West Virginia (WV) Governor Jim Justice in 2019 vetoed Senate Bill 624, which would allow counties to use exams other than the SAT as their 11th-grade standardized test, partly because it “directly conflicts” with existing West Virginia law. This probably propelled WV's SAT participation rate to 99% in 2019. [(source)](https://www.wvgazettemail.com/news/education/governor-vetoes-act-choice-bill-citing-law-requiring-same-test-for-4-years/article_17392d95-a8bb-54b3-89a3-ebbd2e18e841.html) and [(source)](https://www.wvea.org/content/governor-vetoes-act-choice-bill-citing-law-requiring-same-test-4-years)
- In Florida, more students are taking the SAT exam largely because of “SAT school day” programs that allow for taking the exam during the week, at their school, free of charge. Many Florida school districts now offer such programs, driving up SAT's popularity above that of ACT. [(source)](https://www.orlandosentinel.com/news/education/os-ne-sat-scores-florida-20190924-2ycpuogc2ndkrkwzdrkrjgrg64-story.html)

---

### Relationship between Scores & Participation Rates:

![Score vs Participation Rate (ACT)](media/Score_vs_Participation_Rate_(ACT).png)

The 3 linear regression plots above show the relationship beween the ACT participation rate and the state average total score for years 2017 to 2019. As ACT participation rate increases, the average total score generally decreases, indicating an inverse relationship. This observation is generally consistent when we compare these plots from 2017 (left) to 2018 (middle) to 2019 (right), though there may be some outliers.

![Score vs Participation Rate (SAT)](media/Score_vs_Participation_Rate_(SAT).png)

Similar observations can be made in respect of the 3 linear regression plots above that show the relationship beween the SAT participation rate and the state average total score for years 2017 to 2019.

---

### Conclusions:

- The successful combinations of strategies / tactics were gleaned from the various analyses done on both ACT and SAT above, complemented by additional secondary research, and include:
    - Negotiate preferably long term contracts, with optional renewal extensions at same/better terms;
    - (The College Board's) state lobbying efforts and interventions with passing of relevant legislations;
    - Convincing relevant officials to make ACT/SAT compulsory and subsidise test when appropriate;
    - “ACT/SAT school day” programs to allow students to take test for free during the week in school;
    - Increased test frequencies;
    - etc.

- There is generally an inverse relationship between both ACT and SAT scores and their corresponding participation rates. Lower ACT/SAT participation rate typically have higher state average score, and vice versa. This is likely due to biased data in states with low participation rate, as the students who took the test are probably better prepared hence applied for the ACT/SAT voluntarily.

---

### Recommendations:
Having analysed the trends in both the ACT and SAT participation rates above, I have identified the following strategies to improve 2020 ACT participation rates and eventually reclaim ACT's position as the nation’s most widely used college admission test:

- Firstly, I would generally recommend targeting the following stakeholders in decreasing priority:
    - States with no contracts and low participation rates;
    - States with no contracts;
    - States with expiring contract;
    - States with contracts pending renewal and/or extension;
    - State Department of Education;
    - High school administrators;
    - Parents;
    - High School 11th graders;
    - etc.

- Secondly, when negotiating with stakeholders such as State Department of Education and high school administrators, the the preferred terms in decreasing priority are as following:
    - Long term contracts, with optional renewal extensions at same/better terms;
    - Long term contracts;
    - Shorter term contracts, with optional renewal extensions at same/better terms;
    - Shorter term contracts;
    - etc.

- Thirdly, while negotiating with these stakeholders, we shall highlight the relevant additional / optional benefits from the following:
    - ACT's good predictive ability of undergraduate educational performance and success is backed by independent research [(source)](https://www.researchgate.net/profile/Joel-Wao/publication/316554186_SAT_and_ACT_Scores_as_Predictors_of_Undergraduate_GPA_Scores_of_Construction_Science_and_Management_Students/links/590399ab0f7e9bc0d58d7e30/SAT-and-ACT-Scores-as-Predictors-of-Undergraduate-GPA-Scores-of-Construction-Science-and-Management-Students.pdf)
    - Compulsory and Free / Subsidised rates
    - “ACT school day” during the week in school
    - ACT Section Retesting
    - ACT Online testing
    - ACT “superscoring”
    - etc.

- Lastly, the above strategies / tactics should be complemented by ACT's advertising, branding and marketing efforts as follows:
    - Leadership Interviews
    - Roadshows / Tradeshows
    - Seminars / Webinars / YouTube Videos
    - Blog / Guest Posts
    - Press Releases
    - Digital Marketing
    - Banners / Posters
    - TV / Radio / Cable Advertisements
    - etc.

When the above strategies are skillfully executed, I am confident that we stand to potentially improve 2020 ACT participation rates and eventually reclaim ACT's position as the nation’s most widely used college admission test!