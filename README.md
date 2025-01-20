# Keshav_google-play-store-review-analytics
NULL CLASS INTERNSHIP PROJECT

# Task-1 
Create an interactive Choropleth map using Plotly to visualize global installs by Category. Apply filters to show data for only the top 5 app categories and highlight category where the number of installs exceeds 1 million. The app category should not start with the characters “A,” “C,” “G,” or “S.” This graph should work only between 6 PM IST and 8 PM IST; apart from that time, we should not show it in the dashboard itself.
### Libraries used:
pandas,plotly,datetime
### Step-By-Step Plan:
###### 1.Import the Required Libraries:
###### ->Import the necessary libraries for data handling, visualization, and time manipulation.
###### 2.Filter App Categories:
###### ->Exclude categories starting with "A," "C," "G," or "S."
###### ->Keep only the top 5 categories based on the number of installs.
###### ->Highlight categories where the number of installs exceeds 1 million.
###### 3.Create the Choropleth Map:
###### ->Use Plotly's choropleth functionality to map installs by category for each country.
###### ->Use conditional coloring to emphasize categories with installs > 1 million.
###### 4.Restrict Display Time:
###### ->Determine the current time using the datetime module.
###### ->Render the map only if the current time is between 6 PM IST and 8 PM IST.
###### 5.Testing and Deployment: 
###### ->Test the code to ensure the time filter and visualization work as intended.
# Output:
![Image](https://github.com/user-attachments/assets/80dee014-6af8-401a-a570-76c03894e74e)
