


## sources

abstract

https://bigbuild.vic.gov.au/projects

**intro**

https://bigbuild.vic.gov.au/__data/assets/pdf_file/0005/600953/NWNU-Project-Overview-Factsheet.pdf

https://vicroadsopendata-vicroadsmaps.opendata.arcgis.com/datasets/vicroadsmaps::road-crashes-for-five-years-victoria/about

[[road maintence decision making using ahp.pdf]]

[[Combining_cost_benefit_and_multi_criteri.pdf]]

[[SMART_Multi_criteria_decision_making_tec.pdf]]

**problem identification**

https://bigbuild.vic.gov.au/__data/assets/pdf_file/0004/583510/NWNU-Design-Feedback-Digital-Brochure.pdf

https://investment.infrastructure.gov.au/about/local-initiatives/black-spot-program/

[[VicRoads Benefit Management Framework V3.pdf]]

https://www.tmr.qld.gov.au/-/media/busind/businesswithus/existing-infrastructure/smarter-solutions-mca-tool-guide.pdf?la=en

https://www.infrastructureaustralia.gov.au/sites/default/files/2021-07/Assessment%20Framework%202021%20Guide%20to%20multi-criteria%20analysis.pdf

[[rural roads in nigeria.pdf]]

Goodwin chapter 3

SMART paper by Meera Patel again

https://www.vicroads.vic.gov.au/traffic-and-road-use/road-network-and-performance/victorias-road-network

Five-year road crash stats again

https://www.youi.com.au/youi-news/most-common-car-accidents-and-most-dangerous-times-on-the-road

https://discover.data.vic.gov.au/dataset/typical-daily-traffic-volume-profile

https://www.google.com/maps

https://population.gov.au/data-and-forecasts/dashboards/population-local-government-areas

Goodwin chapter 3 again

SMART paper by Meera Patel again

https://www.theguardian.com/australia-news/2023/feb/02/auditor-general-finds-nsw-labor-seats-denied-bushfire-grants-due-to-limit-set-by-john-barilaros-office



## plan

SMART analysis

### problem
Decide which black spot (or generally dangerous) intersection OR road to research upgrades/improvements; why?
- can't do them all, because improvement process is long, including public consultation, drainage, electricity, feasability studies?, impact assessments, etc
- so shortlist the worst blackspots, then do analysis to see which one should be prioritised based on a wide range of safety benefits to maximise value of expenditure

- explain what an upgrade entails; how it is done, how much it costs
- explain how/why these intersections or roads were shortlisted: accident data

### shortlist candidate locations 45min

number of crashes (all severities) per year
https://vicroadsopendata-vicroadsmaps.opendata.arcgis.com/datasets/vicroadsmaps::road-crashes-for-five-years-victoria/about

- [x] then use https://www.google.com/maps to find addresses from accident coordinates
e.g. long = 144.9684, lat = -37.7923 is cnr of lygon and princes sts, carlton


### attributes

- [x] number of fatal injury crashes 15min
	- same source as above
	- all the shortlisted locations, except for one, have 0 fatal crashes, so this attribute likely won't affect the outcome
	- also, creating a value function for a discrete integer scale from 0 to 1 doesn't make sense
	- so discard this attribute

- [x] number of serious crashes 15 min
	- same source as above

- [x] number of other crashes 15 min
	- same source as above

- [x] congestion severity at peak hour 30min
	- https://discover.data.vic.gov.au/dataset/typical-daily-traffic-volume-profile
	- too large to process
	- instead, use google directions to compare travel time at 5pm vs 2am ratio

- [x] proximity to primary schools, hospitals, aged care 30 min
	- https://www.google.com/maps
	- type `primary school nearby` etc
	- e.g. for princes st carlton: hospital 3.5km, primary school 0.6km, aged care 0.5 km
	- then take weighted sum, putting more weight on schools because they have lots of kids in the vicinity, twice a day, every school day

- [x] municipal population (number of people likely to benefit from using it) 15 min
	- https://population.gov.au/data-and-forecasts/dashboards/population-local-government-areas
	- if i had more time i'd look at population density

~~- munipical budget surplus (for resources re consultation and planning)
	- council websites
	- e.g. casey surplus 19/20 was $192.3 M


~~- number of traffic offences per year
	- can't find this so leave it out~~

final attributes as shown in value tree:

![[value tree.svg]]

### assess performance of alternatives

more crashes = "better" i.e. more can be fixed with the money
closer to schools etc = better i.e. more potential improvement in safety
higher population = better i.e. more people experiencing benefits of safer roads

all the attributes are <u>quantifiable</u> so should be assessed using a value function

- [x] create value function for each attribute
- [x] for each alternative, look up the raw data value on the value function for each attribute, and record in a table

![[Pasted image 20230203190313.png]]

some notes on my decisions for the value functions:

[[SMART_Multi_criteria_decision_making_tec.pdf]] contains reference to justification of straight line

serious accidents
- chose 10 crashes as midpoint, as this averages to 2 per year, which i arbitrarily deemed tolerable
- if i had more time, i'd research 'tolerable' levels used in engineering
- the numbers are small, and they're discrete integers, so there are only a few numbers to choose from, so i just chose the medians for the quarter points

other accidents
- chose 12 crashes as midpoint, as this averages to just under 2.5 a year
- then chose medians for quarter points

congestion factor
- chose 3 as the midpoint
- then medians for quarter points

proximity to vulnerable populations
- because less proximity is more pressing to deal with, set value = 0 for the maximum proximity, and value = 100 for the minimum proximity
- chose 3 as the midpoint, as i'd be comfortable with say a school being 3km away
- then medians for quarter points

local population
- chose 200 as the midpoint
- chose 150 for the lower quarter point; there are many LGAs in this ball park, so it doesn't matter that much, and the median would have been almost the same (151.5)
- chose 300 for the upper quarter point, as this is a very large population for an LGA, and i wanted to ensure it got a high value (median would've been 328)

![[Pasted image 20230203233104.png | 650]]

### assign weights to attributes

![[Pasted image 20230204022600.png | 500]]

### evaluate performance of alternatives and make decision

![[Pasted image 20230204022700.png]]

### sensitivity analysis

scenarios:

- weight for serious accidents changes; important to check because it's weighted so heavily
- weight for congestion changes; important to see impact of this attribute because traffic congestion may become a political issue
- weight for population changes; political advisors may prioritise this attribute to attract more votes by focusing investment on more populous areas

- [x] serious accidents
- [x] congestion
- [x] population

