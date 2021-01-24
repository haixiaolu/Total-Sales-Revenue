# [Total-Sales-Revenue](https://haixiaolu.github.io/Total-Sales-Revenue/index.html)
Predict how much sales revenue can be expected from each customer based on their website site visit behaviors 
- **NOTE:** This is a solo project which held on an internal competition between each classmate on Kaggle privately. 
- **Check the HTML Notebook** [here](https://haixiaolu.github.io/Total-Sales-Revenue/index.html)

## Background
In many businesses, identifying which customers will make a purchase (and when) and how much will they spend, is a critical exercise. This is true for both brick-and-mortar outlets and online stores.

## Data 
The data provided in this challenge is website traffic data acquired from an online retailer which collected by our professor **Dr. Charles Nicholson** 

## The Challenge: Predict total sales
The data provides information on customer's website site visit behavior. Customers may visit the store multiple times, on multiple days, with or without making a purchase. The goal is to predict how much sales revenue can be expected from each customer. The variable **revenue** lists the amount of money that a customer spends on a given visit. The goal is to predict how much money a customer will spend, in total, across all visits to the site, during the allotted one-year time frame (August 2016 to August 2017).

## The Results:

| Model       | Method        | Package        | Selection       | Hyperparameter      | R^2       | RMSE        |
| :---        |   :---:       |     :---:      |     :---:       |       :---:         |   :---:   |   :---:     | 
| OLS         | lm            | stats          | step backward   | NA                  | 0.6300    | 1.238       |
| Lasso       | Lasson(small) | elasticnet     | 0.07            | fraction            | 0.6301.   | 1.2388      |
| Ridge       | ridge         | glmnet         | 0.001           | lambda              | 0.6301    | 1.2387      |
| PLS         | pls           | pls            | 10              | components          | 0.6297    | 1.2392      |
| ENR         | Elastic net   | glmnet         | 0.21, 0.006     | alpha, lambda       | 0.6299    | 1.2389.     |

## The approaches and problems that I had along the way

I	did	try	to	use	model	stacking	to	improve	my	model	performance	when	I	built	my	base	
model.	I	updated	seven	different	models	based	my	base	model. Although,	I	made	a	few	
adjustments	and	it	improved	my	scores	from	0.96	to	0.89. I	guess	I	don’t	have	any	secret	
sauce	based	on	my	Kaggle	scores	since	my	score	wasn’t	that	great.		However,	My	best	
performing	model	is	using	backward	stepwise	to	find	the	features	that	related	most.	I	
adjusted	my	model	so	many	times.	

- My	first	approach was using	all	the	features	built	the	
base	model,	and	I	used	stepwise	regression	to	automatically	filter	out	less	important	
features.	Then,	I	compared	my	base	model	and	stepwise	regression model	to	see	which	one	was	performing	better.	

- My	second	approach was	using	cross-validation	and	resampling,	
such	as	during	my	lasso	regression	and	partinal	least	squares	modeling,	I	used	nfolds	and	
number	of	resampling	to	train	my	model.	

- My	third	approach was	adding	new	features	to	
the	data	set	and	using	both	first	and	second approaches	repeatly	to	train	my	models.	I	had	
so	many	problems	during	my	modeling	process,	most	of	them	were	related	my	lack	of	R	
programming	knowledge.	I	got	so	many	different	errors	when	I	tried	to	run	my	scripts.	
Google	and	TA	indeed	helped	me	so	much	for	sorting	thing	out.	Another	difficult	problem	
was	understanding	the	different	modeling	techniques	and	processing	conceptually,	I	have	
to	go	back	to	watch	the	videos	over	and	over	again.	
