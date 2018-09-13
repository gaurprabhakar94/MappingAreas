# MappingAreas
With all the three analysis in this repo, our objective is to dentify and map areas of interest.


1. In both the 'MappingCallRecordsWeekdays' and 'MappingCallRecordsWeekends' analysis, we try to identify the areas of interests of the users based on their phone usage, day of the week and time of the day on which they are using it. The analysis also helps understand exactly how useful is telephone metadata.

	Analysis for the above two is based on the following assumption: 

	On Weekends:

	1. People probably don't go into work
	2. They probably sleep in late on Saturday
	3. They probably run a bunch of random errands, since they couldn't during the week
	4. They should be home, at least during the very late hours, e.g. 1-4 AM

	On Weekdays:

	1. People probably are at work during normal working hours
	2. They probably are at home in the early morning and during the late night
	3. They probably spend time commuting between work and home everyday

	Now, by making use of de-anonmized CDR data and the above assumptions, we find the predictable manners of users moving from home to work with a few errands in between. We then run a K-Means model on the data to isolate the geolocations where a user spends most of his/her time.


2. In the 'MappingCrimeAreas' analysis, we we first start by navigating over to the City of Chicago's Crimes dataset and focus on the crime Gambling. We then train a KMeans model to pin point the areas in the city that a police officer should investigate to check for on-going illegal activities. 