
## plan

#### problem
Decide which black spot (or generally dangerous) intersection OR road to research upgrades/improvements; why?
- can't do them all, because improvement process is long, including public consultation, drainage, electricity, feasability studies?, impact assessments, etc
- so shortlist the worst blackspots, then do analysis to see which one should be prioritised based on a wide range of safety benefits to maximise value of expenditure

- explain what an upgrade entails; how it is done, how much it costs
- explain how/why these intersections or roads were shortlisted: accident data

#### shortlist candidate locations

number of crashes (all severities) per year
https://vicroadsopendata-vicroadsmaps.opendata.arcgis.com/datasets/vicroadsmaps::road-crashes-for-five-years-victoria/about

then use https://www.google.com/maps to find addresses from accident coordinates
e.g. long = 144.9684, lat = -37.7923 is cnr of lygon and princes sts, carlton

then mark them all on a map and save the image

#### attributes

- number of fatal injury crashes 
	- same source as above
	- count how many of each shortlisted node ID

- number of non-fatal injury crashes
	- same source as above
	- count how many of each shortlisted node ID

- congestion severity at peak hour
	- https://discover.data.vic.gov.au/dataset/typical-daily-traffic-volume-profile
	- too large to process
	- instead, use google directions to compare travel time at 5pm vs 2am ratio

- proximity to primary schools, hospitals, aged care
	- https://www.google.com/maps
	- type `primary school nearby` etc
	- e.g. for princes st carlton
	- hospital 3.5km
	- primary school 0.6km
	- aged care 0.7 km

- municipal population (number of people likely to benefit from using it)
	- https://population.gov.au/data-and-forecasts/dashboards/population-local-government-areas
	- if i had more time i'd look at population density


- munipical budget surplus (for resources re consultation and planning)
	- council websites
	- e.g. casey surplus 19/20 was $192.3 M


- number of traffic offences per year
	- can't find this so leave it out





