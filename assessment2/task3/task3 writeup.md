
## plan

SMART algorithm


#### problem
Decide which black spot (or generally dangerous) intersection OR road to research upgrades/improvements; why?
- can't do them all, because improvement process is long, including public consultation, drainage, electricity, feasability studies?, impact assessments, etc
- so shortlist the worst blackspots, then do analysis to see which one should be prioritised based on a wide range of safety benefits to maximise value of expenditure

- explain what an upgrade entails; how it is done, how much it costs
- explain how/why these intersections or roads were shortlisted: accident data

#### shortlist candidate locations 45min

number of crashes (all severities) per year
https://vicroadsopendata-vicroadsmaps.opendata.arcgis.com/datasets/vicroadsmaps::road-crashes-for-five-years-victoria/about

- [x] then use https://www.google.com/maps to find addresses from accident coordinates
e.g. long = 144.9684, lat = -37.7923 is cnr of lygon and princes sts, carlton

- [ ] then mark them all on a map and save the image

#### attributes

- [x] number of fatal injury crashes 15min
	- same source as above

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
	- e.g. for princes st carlton
	- hospital 3.5km
	- primary school 0.6km
	- aged care 0.5 km

- [x] municipal population (number of people likely to benefit from using it) 15 min
	- https://population.gov.au/data-and-forecasts/dashboards/population-local-government-areas
	- if i had more time i'd look at population density


~~- munipical budget surplus (for resources re consultation and planning)
	- council websites
	- e.g. casey surplus 19/20 was $192.3 M


~~- number of traffic offences per year
	- can't find this so leave it out~~

#### assess performance of alternatives

more crashes = "better" i.e. more can be fixed with the money
closer to schools etc = better i.e. more potential improvement in safety
higher population = better i.e. more people experiencing benefits of safer roads





