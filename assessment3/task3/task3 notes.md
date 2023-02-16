# planning

introduce a <u>new</u> fund
- X hours of ES salary per qualifying student
- number of qualifying students is estimated from naplan
- justify the need for this
	- evidence/articles on lack of support staff etc
	- evidence on why X hours of salary

to calculate total pool of money:
- find out how much govt funding the local private schools are getting
- for each school, find the difference between the SRS and how much the school is getting 
- this difference is the funding - redistribute this as the new fund

design decisions - justify each one
- why casey only
- why secondary schools only
- why target private schools for redistribution of funds

constraints - justify each one
- minimum allocation per school = XXXX
- sum of money allocated to all schools <= total funding pool
- state funding + fed funding + new ES funding <= SRS (maybe don't include this; see how it plays out)


# data collection

need to know:

- [x] which secondary schools - private and public - exist in casey
- [x] for private schools, total funding including fees
- [x] SRS i.e. how much it actually costs to educate a child for a year 2020
- [x] total number of students in 2020
- [x] proportion/number of poorly performing students in naplan, for all schools public and private
- [x] ratio of students to non-teaching staff
- [x] total funding pool for new program = private funding in excess of SRS
- [x] ES salary

notes:
- used 2020 data for funding and enrolments as 2020 is the most recent available for the funding, and the enrolments is going to be combined with the funding, so decided to use 2020 for that, too (despite 2022 being available)
- some schools include primary years; no data to separate
- chose to compare naplan results against all australian schools, not just similar ones
	- wanted an absolute measure not a relative one
- filled in missing values with medians of rest of column
- didn't want to completely remove these schools because it would have changed the problem - total funding pool shared among fewer schools

# IP model

### decision variables

x<sub>1</sub> = number of FTE ES staff allocated to school 1
x<sub>2</sub> = number of FTE ES staff allocated to school 2
...
x<sub>13</sub> = number of FTE ES staff allocated to school 3

### parameters

use collected data to formulate parameters:
- [ ] total available budget
- [ ] initial ratio of enrolled students to ES staff
- [ ] % of below average to average naplan results
- [ ] VCE underperformance loading

### objective function

maximise ratio of under-performing students to allocated ES staff

### constraints

- total expenditure <= budget
- final ratio of ES staff to enrolled students <= 25
- number of assigned ES staff >= VCE underperformance loading

# research

### overview and school search

https://www.vic.gov.au/find-your-schools-funding

![[Pasted image 20230215045932.png | 600]]
so demographic data are mostly used?
would using actual performance data affect the allocation?

![[Pasted image 20230215050032.png | 600]]
constraints

### govt guide on funding allocation

https://www.education.vic.gov.au/PAL/student-resource-package-indicative-guide-2023.pdf

two branches of funding:
- core student learning allocation funding
- equity funding

![[Pasted image 20230215051838.png | 600]]
so NAPLAN is used - except the year 5 result is always used, even 6 years later in year 12
this seems crude
would it make a difference to take the latest NAPLAN instead?

![[Pasted image 20230215053256.png | 600]]
this is a pull-out-of-class program
but there is a shortage of ES staff working with kids in their normal classes
that's why my idea is different to the TLI

funding for ES staff is currently part of the PSD (program for students with disabilities)
the PSD fund can be used for:
![[Pasted image 20230215054050.png | 600]]
an amount is given for each student who qualifies, so it is targeted to individual students

but the issues with the PSD are:
- there's no dedicated funding for ES staff; the block of funding is shared across multiple expenditures
- PSD is for students with high needs, but there are lots and lots of students who wouldn't qualify but who are regularly underperforming and behind
	- strict criteria with diagnoses [[psdguidelines.docx]]
	- but i know my school was stretching the ES staff for the funded kids across the unfunded ones too
- schools with PSD funding get less catch-up funding

my idea can improve things because it focuses on performance, to capture all kids who need support, not the just ones with a moderate-severe diagnosis, due to
- poor exec function due to adhd (not mentioned in the PSD criteria and guidelines at all!) - find stats for prevalence of adhd in population AND effect of ADHD on student performance (research papers)
- trauma background (this is not captured by the demographic data used for other equity loadings)
- family problems (also not directly captured, other than financial hardship)
- mental illness

![[Pasted image 20230215060739.png | 600]]
but how, if the funding isn't there??


### policy on equity funding

https://www2.education.vic.gov.au/pal/student-resource-package-srp-equity-funding-student-based-funding/policy


### policy on core student learning allocation funding

https://www2.education.vic.gov.au/pal/srp-core-student-learning-allocation/policy


### save our schools research paper

education research paper
https://saveourschools.com.au/funding/the-facts-about-school-funding-in-australia/

public schools only get 91% of their SRS at best
private schools get *over* 100%


### fed govt SRS explainer

https://www.education.gov.au/recurrent-funding-schools/schooling-resource-standard

![[Pasted image 20230215061324.png | 600]]
this is shocking

[[ESE21-0486 AG Schools Funding Report_ACC.pdf]]
![[Pasted image 20230215132614.png | 650]]
but remember, govt schools only get 20% of this amount

SRS has additional loadings for
![[Pasted image 20230215061558.png | 400]]

![[Pasted image 20230215061707.png | 600]]


### schools in casey

https://data.casey.vic.gov.au/explore/dataset/primary-and-secondary-schools/

https://data.casey.vic.gov.au/explore/dataset/primary-and-secondary-schools/information/
metadata about this dataset

### CTC (capacity to contribute) scores for non-gov schools

[[capacity_to_contribute_scores_for_non-government_schools_for_2020-final.pdf]]
metadata for 2020
![[Pasted image 20230215131912.png | 600]]

https://www.education.gov.au/school-funding/estimator
![[Pasted image 20230215131339.png | 600]]


### ISA info on SRS funding

https://isa.edu.au/our-sector/funding/school-funding-model/


![[Pasted image 20230215120919.png]]

### ACARA sources

school profiles
https://www.acara.edu.au/contact-us/acara-data-access

naplan dictionary
https://www.acara.edu.au/docs/default-source/default-document-library/naplan-results-data-dictionary-2021.pdf

individualised school funding and naplan data
https://www.myschool.edu.au/

### education support salaries in vic

https://www.education.vic.gov.au/hrweb/Documents/Salary-EducationSupportClass.pdf

level 1, range 2-8
10 years' experience
salary as at 1/1/23: $68,943

level 2, range 2-3
5 years' experience
salary as at 1/1/23: $57,975

### VCE performance

https://www.vcaa.vic.edu.au/administration/research-and-statistics/Pages/SeniorSecondaryCompletion.aspx

