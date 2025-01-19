# Web Scraping Atlanta Restaurants with Yelp API & Visualizing Data in Tableau

This project demonstrates how to collect and visualize restaurant data from Yelp using web scraping techniques (through the Yelp API). The data, which includes restaurant names, ratings, locations, reviews, and categories, is retrieved from Yelp’s API, saved in CSV format, and visualized using Tableau.

## Project Overview
The goal of this project is to simulate a web scraping process by leveraging Yelp’s API to extract valuable restaurant data for Atlanta. The data is then saved as CSV files, which can be imported into Tableau for creating interactive visualizations.

**View the Tableau Dashboard**  
   You can view the final Tableau dashboard using the following link:  
   [View the Dashboard](https://public.tableau.com/app/profile/fnu.sagarika/viz/YelpAtlanta/Dashboard)

## Features

- Fetch restaurant data from the Yelp API for Atlanta.
- Collect detailed information about restaurants, such as:
  - Name
  - Rating
  - Location (Address, Latitude, Longitude)
  - Phone number
  - Categories
  - Number of reviews
- Visualize data using Tableau for interactive insights.
- Aggregate category counts to create a petal chart (or other visualizations in Tableau).
- Data is stored in CSV format for further analysis.

## Technologies Used

- **Yelp API**: To fetch restaurant data.
- **Python**: For processing the data (requests, CSV writing).
- **Tableau**: For building the interactive dashboard.
- **CSV**: To store data locally for later visualization.


 **Get Yelp API Key**  
   - Go to Yelp's Developer Portal and sign up to get an API key.
   - Replace the placeholder `#` in the code with your actual API key.

**Run the Python Script**  
   After replacing the API key, run the Python script to fetch the data.
   This will generate a CSV file named `atlanta_restaurants_full.csv` containing the restaurant data.

**Upload the CSV to Tableau**  
   Use Tableau to import the `atlanta_restaurants_full.csv` file and create your interactive dashboard.


## Code Explanation

### `fetch_yelp_data.py`
This script connects to the Yelp API and retrieves restaurant data based on the search term "restaurants" and location "Atlanta, GA". It loops through multiple pages of results (up to 200), extracts necessary information, and writes it into a CSV file.

### Data Aggregation for Visualization
A second script aggregates the categories of the restaurants to create a summary for visualization, which is saved in a separate CSV file (`atlanta_restaurants_petal_chart.csv`) for use in creating charts like petal charts in Tableau.

## CSV Data Structure

### `atlanta_restaurants_full.csv`
- **RestaurantName**: Name of the restaurant.
- **Address1**: Full address of the restaurant.
- **RestaurantCity**: City of the restaurant (fixed as "Atlanta").
- **Phone**: Phone number (if available).
- **Latitude**: Latitude of the restaurant.
- **Longitude**: Longitude of the restaurant.
- **URLTag**: Yelp URL of the restaurant.
- **AvgRating**: Average Yelp rating of the restaurant.
- **NoReviews**: Total number of reviews.
- **Category**: List of categories assigned to the restaurant.

### `atlanta_restaurants_petal_chart.csv`
- **Category**: Category of the restaurant.
- **CountOfCategory**: Number of restaurants in that category.
- **Path**: Used for visualization purposes.


## Acknowledgements

- Thanks to Yelp for providing the API to access restaurant data.
- Special thanks to Tableau for their powerful data visualization tool.
  
---

Feel free to customize this README as needed!
