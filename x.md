ZZCA6510 3: Prescriptive Decision Analysis  
Amanjit Gill  
February 21, 2023

1 Product Composition  
Peanut for Life, a food manufacturer, seeks to produce a chanachur snack product comprising  
three mixtures: puffed rice, nuts and cereal. Each ingredient mixture has a different cost per  
kilogram (see Table 1); therefore, Peanut for Life is aiming to minimise the total cost of each  
package of chanachur by formulating a linear programming model.  

If x1, x2 and x3 represent the weight (in kilograms) of puffed rice, nuts and cereal respec-  
tively, then the total cost of one package of chanachur would be:  
total cost = 0.35x1 + 0.5x2 + 0.2x3 (1)  
The objective is to minimise this quantity. However, there is not just the cost to consider.  
Peanut for Life must also ensure the product is commercially viable; it can do this by composing  
the product in such a way that it is both nutritionally balanced and attractive to consumers.  
To this end, the following constraints on the final composition are given:  
• The chanachur package must hold between 3 and 4 cups of product.  
• One package cannot contain more than 1000 calories in food energy.  
• One package cannot contain more than 25 grams of fat.  
• At least 20% of the product volume must comprise puffed rice mixture.  
• No more than 15% of the product weight may comprise nuts.  
Using the nutritional information provided in Table 2, these constraints may be modelled  
mathematically as inequalities 2 to 7, presented in canonical form.  

−0.25x1 − 0.375x2 − x3 ≤ −3 (2)  
0.25x1 + 0.375x2 + 1x3 ≤ 4 (3)  
150x1 + 400x2 + 50x3 ≤ 1000 (4)  
10x2 + 1x3 ≤ 25 (5)  
1

−0.2x1 + 0.075x2 + 0.2x3 ≤ 0 (6)  
−0.15x1 + 0.85x2 − 0.15x3 ≤ 0 (7)  
One additional constraint is required; that is, a nonnegativity constraint for the weight of  
each ingredient:  
xi ≥ 0, where i ∈ {1, 2, 3} (8)  
Equation 1, together with inequations 2 to 8, completely define the linear programming  
model for optimising the composition of the new chanachur product. However, when it is solved  
using the Simplex algorithm, the optimal solution does not include any nuts at all. This is likely  
due to the high fat and energy content of the nut mixture (as shown in Table 2) encouraging  
the solver to favour the less nutritionally dense puffed rice and cereal mixtures.  
From a marketability standpoint, this is an unacceptable result, as nuts cannot be excluded  
from a commercially viable chanachur product. For this reason, a minimum amount of nut  
mixture must be enforced through an additional constraint. A cursory examination of popular  
chanachur recipes reveals that most small batches contain between 0.5 and 1.0 cups of nuts;  
approximately 75-113 grams. Therefore, for the present exercise, a nominal minimum of 100  
grams has been chosen, and represented by inequation 9 in canonical form.  
−x2 ≤ −0.1 (9)  
When the model is solved with this new constraint, a more suitable composition is achieved.  
This is given in Table 3. The corresponding minimal cost per package is $1.36.  


2 Staff Scheduling  
Chris Stokes, the rostering manager at Orient Computer Manufacturer, has been tasked with  
developing a staff schedule that minimises the total weekly cost of salary payments. Employees  
at Orient work in weekly shifts that include two days off, and their weekly salary depends on  
which days they are rostered on, as shown in Table 4. In addition, Mr Stokes has estimated the  
number of workers required on the factory floor every day of the week; this is shown in Table 5.  

Mr Stokes sees that a linear programming approach is ideally suited to this scenario. To  
this end, if x1 represents the number of employees assigned to shift 1, x2 represents the number  
of employees assigned to shift 2, and so on, then the total salary cost for one week would be:  
total salary = 900x1 + 850x2 + 920x3 + 860x4 + 780x5 + 910x6 + 850x7 (10)  
The objective is to minimise this cost while ensuring that the staff requirement for every  
day is met. This can be done by representing the number of workers required every day, given  
in Table 5, as a set of constraints. These manifest themselves as inequations 11 to 17.  
x2 + x3 + x4 + x5 + x6 ≥ 18 (11)  
x3 + x4 + x5 + x6 + x7 ≥ 13 (12)  
x1 + x4 + x5 + x6 + x7 ≥ 15 (13)  
x1 + x2 + x5 + x6 + x7 ≥ 18 (14)  
x1 + x2 + x3 + x6 + x7 ≥ 21 (15)  
3
x1 + x2 + x3 + x4 + x7 ≥ 18 (16)  
x1 + x2 + x3 + x4 + x5 ≥ 21 (17)  
There are additional constraints; namely, that each five-day shift must be assigned at least  
one worker, and that the number of workers assigned to each shift is a nonnegative integer.  
While part-time assignments are possible in other scenarios, Orient states that its employees  
are entitled to two days off per week, implying that its entire staff body works full time i.e. five  
days per week.  
The additional constraints are represented by inequations 18 and 19. It is also conventional  
to explicitly require nonnegativity (see inequation 20) but inequation 18 is sufficiently restrictive.  
xi ≥ 1, where i ∈ {1, 2, .., 7} (18)  
xi ∈ Z, where i ∈ {1, 2, .., 7} (19)  
xi ≥ 0, where i ∈ {1, 2, .., 7} (20)  
The objective function, given by equation 10, together with these constraints form a complete  
mathematical model suitable for linear programming. When this model is solved, an optimal  
number of employees working each five-day shift is obtained (see Table 6). The corresponding  
minimal salary cost is $22,410.  


3 Independent Analysis  
3.1 Executive Summary  
3.2 Introduction  
The purpose of this analysis is to formulate a new method, involving linear programming prin-  
ciples, by which funding can be allocated to public schools, in such a manner that emphasises  
support for students who underperform academically due to disability or social factors.  
This study specifically focuses on public secondary schools in a single municipality, the City  
of Casey in Victoria. The scope has been such limited for the following reasons:  
• Because this study aims to function as a proof of concept, it is desirable to limit its scope  
to a small subset of schools, as this allows the efficacy of the proposed methodology to be  
demonstrated without the complexity inherent in larger scale modelling.  
• Eliminating primary schools from the analysis removes the possibility that uncontrolled  
differences between the primary and secondary school systems might affect the results and  
conclusions.  
• Confining the analysis to a single municipality, the City of Casey, eliminates any possible  
influence of demographic differences between municipalities.  
Students who require extra support at school are sometimes provided access to Education  
Support (ES) workers. These roles are filled by paraprofessionals who do not perform a teaching  
role and who are usually not degree-qualified educators. Because of this, they are counted among  
“non-teaching staff”. Publicly available data from ACARA (Australian Curriculum, Assessment  
and Reporting Authority, 2022b) show that for non-government schools, the median ratio of  
enrolled students to non-teaching staff is much lower than for government schools. Table 7  
shows these ratios for the City of Casey.  
Table 7: Median ratio of students to non-teaching staff in Casey.  
Sector Median Ratio  
non-government 21  
government 34  
These figures suggest that in the public education sector, funding and provision of non-  
teaching staff, including ES workers, may be falling short of demand, and that students at  
non-government schools may be better-serviced than those in government schools. In order to  
understand why this may be happening, it is instructive to examine how schools in Victoria -  
and Australia generally - are funded.  
State governments are largely responsible for funding public schools, although the federal  
government also contributes a smaller amount. Each year, the federal government calculates  
the SRS (Schooling Resource Standard), which is the amount it costs to educate a child for one  
year (Australian Government Department of Education, 2023). In 2020, the base SRS amount  
was $14,761 for secondary students (Australian Government Department of Education, Skills  
and Employment, 2021).  
After adjusting for school-specific “loadings” (ibid.), the federal government provides 20%  
of the SRS amount to government schools, and 80% of it to non-government schools. The  
Victorian government is thus responsible for providing 80% of the SRS amount to government  
schools, and 20% to non-government schools.  
In practice, the Victorian government divides its funding burden into two categories: the  
core student learning allocation (that is, the basic amount allocated to every student) and equity  
5

funding (Victorian Department of Education, 2023). The amount of equity funding a school  
receives depends on the specific demographic and academic profile of the school, and takes into  
account the academic needs of individual students. One type of equity funding comes from the  
PSD (Program for Students with Disabilities). To attract PSD funding to a school, a student  
must meet specific disability criteria, and the allocated amount varies with the severity of the  
disability (Victorian Department of Education, 2022b).  
While this is a sound model in principle, it is problematic for the following reasons:  
• Students with ADHD (Attention Deficit Hyperactivity Disorder) do not qualify for extra  
funding (ibid.). According to Faraone et al. (2021), school functioning is strongly impaired  
by ADHD, a condition common to 5.9% of youths. This means that no children with  
ADHD, who do not meet other criteria under the PSD guidelines, receive any support at  
school, despite conclusive evidence of severe impacts to educational attainment.  
• Research such as that by Blodgett and Lanigan (2018) shows that children with a high  
number of ACEs (adverse childhood experiences) are more likely to suffer poor school  
attendance and poor academic achievement. Unless such children exhibit behavioural  
problems severe enough to meet PSD funding criteria, their underachievement will go  
unnoticed and unaddressed.  
• Even children whose diagnoses meet the PSD criteria are often unable to attract sufficient  
funding. At one school within the City of Casey, a student whose executive functioning  
was severely impaired by Autism Spectrum Disorder was allocated an ES worker for only  
one mathematics lesson per week, meaning he was unable to make any progress for the  
remaining four lessons every week. The lack of access to support for this student, despite  
a confirmed urgent need, indicates that current funding provisions are either inadequate  
or misapplied.  
These observations about the shortcomings of the Victorian government’s PSD are the  
foundation of the present study. They make the case that a more inclusive, targeted, funding  
model is required; one that captures students who would otherwise fail to meet funding criteria,  
and one that provides support that is more proportionate to the needs of students who are  
severely impacted by disabilities.  
School-specific data required for this work have been obtained from government websites,  
while information about state and federal funding models has been obtained from the extensive  
guidelines and documentation published by government education departments. This context-  
specific information has been supplemented by examining research articles about educational  
practices (especially in the context of students with higher needs) and also about the applica-  
bility of linear programming in funding allocation scenarios.  
In collecting data for this analysis, a number of limitations have revealed themselves:  
• There is no publicly available data on what proportion of students are underperforming at  
schools. Data from standardised testing reveal the percentage of students at every school  
whose two-year progress is “above average”, but there is no information on the percentage  
of students whose progress is below average or poor (Australian Curriculum, Assessment  
and Reporting Authority, 2022a). Because of this, it is difficult to estimate the number of  
children at a school who might need support but who fall outside the strict PSD criteria.  
An alternative measure has been formulated - an “academic deficit” score for each school  
(see Section 3.4).  
• A small number of secondary schools in Casey service both primary and secondary year  
levels (City of Casey, 2021). There is no readily accessible data on what proportion of these  
schools’ total enrolment comprises secondary students. The federal government’s SRS  
6

base amount is different for primary and secondary (Australian Government Department  
of Education, Skills and Employment, 2021), so an assumption has been made that all  
of the students at these schools attract the SRS base amount for secondary students,  
regardless of their age. This means that funding estimates for these schools are likely to  
be inaccurate.  
• A small number of secondary schools in the catchment area for this study have only  
recently opened, so there is no NAPLAN (National Assessment Program – Literacy and  
Numeracy) data available for them. In addition, a small number of schools do not offer  
VCE (Victorian Certificate of Education) classes, meaning there is no VCE performance  
data for them. This has been addressed by filling in these missing values with medians  
calculated from the other schools. This is preferable to removing the schools from the  
dataset; there are only 13 government secondary schools in Casey, so removing even one  
or two may significantly alter the funding allocated to the remaining schools.  
These limitations have been mitigated as described above, but will inevitably impact upon  
the accuracy of the figures. Nevertheless, the results of the analysis suggest that linear pro-  
gramming is a valid, efficient, tool for allocation of funding in narrow contexts such as disability  
support, and that significant cost savings are possible if education funding is applied in a more  
targeted way.  
3.3 Problem Identification  
As discussed in Section 3.2, the ratio of enrolled students to non-teaching staff at government  
schools is much higher than at non-government schools (Australian Curriculum, Assessment and  
Reporting Authority, 2022b). This, combined with the aforementioned evidence that students  
with ADHD and ACEs are likely to be underserviced by the PSD, suggests that provision of  
Education Support staff is inadequate at public schools, and that this is not limited to individual  
schools; rather, it may be a system-level deficiency requiring a system-level response.  
In addition to the PSD, the Victorian government has conceived the TLI (Tutor Learning  
Initiative) to address concerns that students have fallen behind due to schooling disruptions  
during the COVID-19 pandemic (Victorian Department of Education, 2022c). This program  
provides a minimum of $25,000 to every government school per year, and this amount is only  
permitted to be used for on-campus tuition services.  
The state government encourages schools to use the TLI funding for small-group tuition,  
which usually involves children being sent out of their regular classes to attend tuition sessions.  
Research such as that by Rea, McLaughlin, and Walther-Thomas (2002) shows that “pull-out”  
programs are not as beneficial as programs in which students are offered additional support to  
remain in their regular classes. Pull-out programs may cause students to fall further behind due  
to their absence from mainstream classes; by constrast, more inclusive programs are associated  
with higher academic achievement and fewer behavioural issues (Rea, McLaughlin, and Walther-  
Thomas, 2002).  
These findings are supported by Reifler (2021), whose study indicates that pull-out programs  
have a negative influence on students’ self-concept and test scores. Therefore, it is proposed  
that the TLI is not a sufficient response to students falling behind, and that a separate program,  
emphasising the use of ES staff to support students in mainstream classrooms, is required in  
addition to - or instead of - the TLI.  
A potential barrier to this proposal is that some teachers may have a negative attitude to  
inclusive practices. While there is very little objection to the principle of inclusion, research  
shows that teachers who are underresourced resent the perceived complication that coordination  
with another educator might add to their daily work (Saloviita, 2020). In addition, ES workers  
themselves complain of lacking confidence in the curriculum material they are expected to help  
7

children to learn, due to a lack of support and training (Poed et al., 2016). These observations  
are not arguments against an increased investment in Education Support; rather, they are  
arguments supporting the provision of time and funding to maximise the value of ES workers  
to both teachers and students.  
Having established that existing measures - such as the PSD and TLI - are not adequately  
supporting students, and that investment in ES workers should be increased, the issue of funding  
allocation (that is, how much money should be given to each school for this purpose) manifests  
itself as a problem in prescriptive analytics. This third phase of analytics, the first two being  
descriptive and predictive (Vigliarolo, 2019), centres on conducting analysis that culminates in  
the recommendation of a specific decision (or decisions) to optimise some stated objective. In  
the present case, the allocation of ES funding to schools must be done in such a way as to  
be financially sustainable, meaning there is an objective to meet students’ needs for support  
while minimising the cost to taxpayers. In Section 3.4, it shall be shown how this prescriptive  
analytics problem can be expressed validly as a linear program.  
3.4 Solution Approach  
Linear programming has been confirmed as the preferred prescriptive analytics approach because  
it allows the requirements of the schools seeking disability support staff to be balanced with the  
imperative to allocate public funds in a fiscally responsible way. Other potential approaches  
were considered and rejected on the following grounds:  
• For a large-scale project in which funding is allocated for a number of different uses,  
goal programming would be an ideal candidate, because it allows for multiple competing  
imperatives to be balanced against one another. For example, it may be used to distribute  
funding across different priorities such as sports equipment, musical instruments and art  
supplies. Its applicability to academic resource planning also been noted by Tamiz, Jones,  
and El-Darzi (1995). However, given that the present study focuses on only one goal -  
Education Support assistance for underperforming students - goal programming is not  
considered a suitable method.  
• Some consideration has been given to binary programming, a stricter form of linear pro-  
gramming in which each school would either be allocated funding or not, depending on  
a determination of need. While binary programming has been validated for other uses in  
education, such as timetabling (Tripathy, 1984), this would not be a suitable approach for  
the present problem because it would not differentiate between schools requiring large and  
small investments; every chosen school would be designated a value of ‘1’ or ‘0’, regardless  
of its degree of need. By contrast, linear programming in its original form (even when con-  
strained to produce integer results) offers the opportunity to differentiate between schools  
with high needs and low needs.  
With a linear programming approach confirmed as most suitable, one can proceed with  
developing a mathematical model. Firstly, the City of Casey has thirteen public secondary  
schools; each one is assigned a decision variable representing the number of additional ES  
workers that have been allocated to it. These variables are given in Table 8.  
As stated in Section 3.3, the objective of the present exercise is to allocate ES workers  
to public schools in such a way as to minimise the total salary cost. According to Victorian  
Department of Education (2022), the salary for an Education Support worker with ten years’  
experience is $68,943 as at 1 January, 2023.  
The linear program can be substantially simplified by assuming that all assigned ES workers  
will be paid this salary; that is, an assumption can be made that all hired workers will have ten  
years’ experience. Then the objective function is to minimise the total cost given by:  
8


total cost = 68, 943 ×  
13∑  
i=1  
xi (21)  
Because the salary is identical for each theoretical ES worker, the objective could also be  
expressed as a minimisation of the number of hired workers:  
total num hired =  
13∑  
i=1  
xi (22)  
In order for the linear program to produce a fiscally responsible solution, the following  
constraints are required:  
• The total expenditure must be below some nominated budget. In order to determine what  
this bound should be, the recurrent funding available to non-government schools in the  
City of Casey in 2020 has been obtained from the My School website (Australian Cur-  
riculum, Assessment and Reporting Authority, 2022a) and compared against the funding  
required according to the 2020 SRS (Australian Government Department of Education,  
Skills and Employment, 2021). Table 9 shows that in 2020, non-government schools re-  
ceived more than $106 million in excess funds. Given the significant underservicing of  
government schools, these surplus funds should be redistributed to the public system.  
This approach is validated by the observation made by Shehab et al. (2021) that govern-  
ments should consider equity rather equality; that is, they should abort their insistence  
upon providing large amounts of public funds to privately educated students regardless  
of need. With this in mind, the nominated budget for the present analysis is set at  
$106,656,982.  
• In order to avoid a large influx of new workers causing a school’s staffrooms to become  
overcrowded (and thus introducing new problems pertaining to amenity and safety), the  
number of new ES workers allocated to a school should be limited to 25% of the ini-  
tial number of employees at the school. The staffing figures have been obtained from  
Australian Curriculum, Assessment and Reporting Authority (2022).  
• Regardless of whether or not a school needs additional support, the final ratio of enrolled  
students to non-teaching staff should be below 40. While this is still much higher than the  
median ratio of 21 as shown in Table 7 for non-government schools, this bound represents  
9

a reasonable short-term improvement for four out of thirteen government schools; the  
Victorian government should thereafter continue to drive the ratio downwards over time.  
• In order to allocate ES resources fairly, each school should be assigned a deficit score; that  
is, a numerical representation of the extent to which students at the school require addi-  
tional Education Support funding. This deficit score should be normalised so it represents  
the school’s share of the overall “academic deficit” in Casey. Then, the school’s share of  
the total allocated ES funding should at least equal the school’s share of the academic  
deficit.  

In addition to these operational constraints, a nonnegativity constraint applies to all thirteen  
decision variables, as is mandatory for all linear programs. An integer constraint has also been  
applied, to simplify interpretation of the results by limiting the recommended funding allocations  
to whole multiples of a full-time salary.  
The final operational constraints are given by inequations 23 to 26. The data used to  
compute the constants are given in Table 10. Note that the “academic deficit” score for each  
school has been computed by applying the following procedure to NAPLAN data (Australian  
Curriculum, Assessment and Reporting Authority, 2022a) and VCE data (Victorian Curriculum  
and Assessment Authority, 2022):  
1. Obtain the Year 9 raw NAPLAN scores for reading, writing, spelling and grammar. Com-  
pute the mean of these four figures to obtain a single figure for ‘literacy’. Compute the  
difference between this figure and the national average.  
2. Also obtain the Year 9 raw NAPLAN score for numeracy; compute the difference between  
this figure and the national average score for numeracy.  
3. Obtain the median VCE study score for the school. Compute the difference between this  
and the mean, which is always set to 30 every year (Victorian Curriculum and Assessment  
Authority, 2023).  
4. Add up the differences computed in Steps 1 to 3. This is the school’s “academic deficit”.  
Note that a school with no deficit (effectively an “academic surplus”) is assigned a score  
of 0.  
5. Add up all the schools’ academic deficits; divide each school’s deficit by this sum, yielding  
a normalised figure representing the school’s share of the overall academic deficit.  



68, 943  
13∑  
i=1  
xi ≤ 106, 656, 982 (23)  
si  
ni + xi  
≤ 40 (24)  
xi ≥ di  
13∑  
i=1  
xi (25)  
xi ≤ 0.25(ti + ni) (26)  
i ∈ {1, 2, .., 13} (27)  
xi ≥ 0 (28)  
xi ∈ Z (29)  
Note that:  
• si = enrolled students  
• ni = non-teaching staff  
• ti = teaching staff  
• di = academic deficit (normalised)  
It is anticipated that these constraints will yield an optimal salary cost, ensuring schools are  
granted support that is proportional to their needs, while keeping workforce growth sustainable  
to ensure that existing school buildings are capable of supporting an increase in staff numbers.  
It is also anticipated that the total salary cost will be well below the very large $106 million  
nominal budget, showing that emphasising support for underperforming students need not be  
an expensive exercise relative to other government programs.  
3.5 Results and Discussion  
When the mathematical model from Section 3.4 is solved using the Simplex algorithm, the  
optimal number of Education Support workers allocated to each of the thirteen schools is as  
shown in Table 11.  
3.6 Conclusion  



