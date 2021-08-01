# World Weather Analysis

Weather Analysis created for a travel app, "PlanMyTrip"

## Results

### Retrieving Weather Data
To create the best customer experience, I randomly generated 2000 latitudes and longitudes and populated a list of cities from the coordinates. Using the list of cities, a large dataframe of the city information was created using OpenWeather API and a for loop with a json request for each city's information. A try-except function was including the code to skip over cities that caused any errors. 

Below is the beginning of the dataframe created.
![WeatherDatabase](https://user-images.githubusercontent.com/84139177/127783484-f003ba4b-e23a-4659-830b-204db609d8cc.png)

### Creating a Customer Travel Destinations Map
The city dataframe was necessary for the next step, which was to create an interactive map of destinations for the customer. First, an input code was created to let the customer choose which kind of weather they would prefer for their destination based on the highest and lowest temperature they liked. With the customer's preferred maximum and minimum temperature data stored, a "preferred" city dataframe was created from the initial city dataframe.

![PreferredCitiesDF](https://user-images.githubusercontent.com/84139177/127783594-ee319fc0-c1a4-4407-9f87-d10882da1853.png)

Then, using a Google Maps API, a hotel was found for each city in the preffered database based on the city coordinates. This hotel information was added to the preferred city dataframe. Using a marker layer on google maps, I then created an interactive map that allows the customer to see which cities fall into their preferred weather category and learn unique information about each city.

![WeatherPy_vacation_map](https://user-images.githubusercontent.com/84139177/127783707-b328ef8f-a856-421a-a054-f740607eb2b5.png)

### Creating a Travel Itinerary Map
Going one step further, I created an option to create an travel itenerary from their preferred cities. Using the vacation dataframe created previously, I came up with an imaginary trip around the Chicago area, using three pit stops for my data. Using the coordinates of the cities, I made a direction map with Google Maps.

![Travel code](https://user-images.githubusercontent.com/84139177/127783948-924cab8c-6f7c-4931-a838-5d7cb07b221b.png)
![WeatherPy_travel_map](https://user-images.githubusercontent.com/84139177/127783994-5aab4615-a414-4dc8-8891-246f67304823.png)

Additionally, a map with information markers was made after combining the itinerary city information into a dataframe. 

![WeatherPy_travel_map_markers](https://user-images.githubusercontent.com/84139177/127784013-2a95400f-4c0f-4765-a7ef-65e83547b441.png)

## Future Considerations
There are many directions for the travel app to take. I would like to see more input options available for the customer, like "which country would you prefer?" Questions like, "what do you like doing on your vacation (swimming, skiing, etc.)?" can be asked by added additional data to the dataframe based on nearby attractions and activities. 

Lastly, additional helpful information can be provided to the customer on the interactive maps, such as booking and hotel website information. However, websites can become obsolete so, if links were included, additional care would need to be taken to regularly ensure that the data collected is up to date.
