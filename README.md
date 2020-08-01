# capstone-coursera-IBM-datascience


New Brewery Opening Location


1.	Introduction:

As part of the IBM capstone project, I have chosen an idea related to opening a new Brewery in a location of my preference i.e. Bangalore.
Bangalore is famous for its pubs, bars and brewery culture. So, this got me interested in finding out what locations/neighborhoods in Bangalore would be
suitable for opening a new brewery or a branch of an existing brewery.

One of the motivations for choosing this problem statement is related to my preference for brewed beer vs bottled beer – I occasionally do enjoy bottled beer,
but given a choice I would choose freshly brewed. Also, in case of brewed beer there are many options in terms flavors and concentrations to choose from.
And I am seeing an increasing trend in this behavior and will result in many new breweries opening with more variations in their menu.

From the business point of view, the location of an outlet can make or break decision. Many factors contribute to the success of running bar, pub or brewery.
Primary being the location/neighborhood, and others include surrounding venues, type of crowd in the neighborhood, main landmarks etc.
So, in this project, I will using clustering concept to find the best possible locations in Bangalore to open a Brewery.

2.	Data acquisition:

For any data science project, the quality of data is more important than the quantity of data. The key data that I will be using in this project is the location data of Bangalore
neighborhood i.e. longitude and latitude of key places. Along with this to fetch venue details of places around these neighborhoods, I will be using the Foursquare APIs.
Below is snapshot of the location data of Bangalore neighborhood. It contains neighborhood name, pin code, zone (east, west etc.), longitude and latitude.
I have acquired this data by web scraping mechanism. 

 

Along with this, I would be using the venues information in and around these neighborhoods. That will look like something like shown below.
Using the Foursquare API, I will be getting all the venues belonging to different categories like parks, temples, schools, restaurants, café, bars etc.

  

One important consideration to keep in mind is that I am looking for neighborhoods suitable to open new beer brewery. As a result, below aspects have been 
kept in mind while data cleaning and filtering.
•	Beer Brewery business can thrive in places where there is already a hub of eateries, bars, pubs and other breweries.
•	This indicates that people these neighborhoods are already having preference for eating and drinking out.
•	Or these neighborhoods have other aspects, like a shopping mall, IT parks or movie halls, that is attracting people.
•	Adding to this, people would want to have options in terms of their dinning/drinking experience. So, looking out for such neighborhoods can add value
since a new place might get a preference.
•	Also starting a brewery in a place that doesn’t have any good concentration of food and drink places might be risky.
•	So, I would be filtering data to remove other category venues.
•	As a result, in each neighborhood, I would be interested in venues that belong these venue categories:  restaurants, bars, cafes, pubs, breweries etc...


3.	Methodology 

The problem I am trying to solve here is identifying the suitable location in a city to open a new beer brewery. Whether it is a restaurant or café or any other eatery
location matters a lot. Using the location data of neighborhoods and venue information, I would be able to build clusters of neighborhoods having similar characteristic.
As discussed in the data acquisition section, I would be filtering to acquire right set of venue categories. The right way to go about analyzing the neighborhoods of a city
is to use the similarity in the venues hosted by them. Using the presence of venues of different categories and their mean occurrence in the neighborhood I can build cluster
of neighborhood with similar venue categories. 

K-means algorithm is best suited for this problem with such requirement. Using this algorithm, I have created clusters with similar characteristics in terms of the venues hosted
by them.  I have used the Elbow method to find optimal K in K-means, and it comes to be 4. 


					 

					The below maps show the neighborhood before and after the cluster.
													Before																	After
					  

4.	Results 

Once the clustering was done, I spent time analyzing each cluster. Of the all the clusters, one had the rich mix of venues related for food and drinking,
Below we can see that cluster 3 is right candidate and we will analyze further. Right candidate because, it has lot of varied restaurants, bar, pubs breweries.
In this cluster we will try to find out is there any neighborhood that doesn’t have a brewery. And that neighborhood would one of the ideal candidate for opening
new brewery.

   

 

On further analysis I found that there are two neighborhoods in this cluster that doesn’t have a brewery but have a pubs , bars and restaurants.
 

5.	Conclusion

As discussed above we can see that using the location data of Bangalore neighborhoods and also the venue information from Foursquare API,
I was able to create cluster of neighborhood that have mix of restaurants, bars,cafe,pubs etc..
And on further analyzing , I was able to get to the neighborhoods that are suitable to host new Brewery.



