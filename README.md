# Keshav_google-play-store-review-analytics
NULL CLASS INTERNSHIP PROJECT

# Task-1 
Create an interactive Choropleth map using Plotly to visualize global installs by Category. Apply filters to show data for only the top 5 app categories and highlight category where the number of installs exceeds 1 million. The app category should not start with the characters “A,” “C,” “G,” or “S.” This graph should work only between 6 PM IST and 8 PM IST; apart from that time, we should not show it in the dashboard itself.
### Libraries used:
pandas,plotly,datetime
### Step-By-Step Plan:
##### 1.Import the Required Libraries:
###### ->Import the necessary libraries for data handling, visualization, and time manipulation.
##### 2.Filter App Categories:
###### ->Exclude categories starting with "A," "C," "G," or "S."
###### ->Keep only the top 5 categories based on the number of installs.
###### ->Highlight categories where the number of installs exceeds 1 million.
##### 3.Create the Choropleth Map:
###### ->Use Plotly's choropleth functionality to map installs by category for each country.
###### ->Use conditional coloring to emphasize categories with installs > 1 million.
##### 4.Restrict Display Time:
###### ->Determine the current time using the datetime module.
###### ->Render the map only if the current time is between 6 PM IST and 8 PM IST.
##### 5.Testing and Deployment: 
###### ->Test the code to ensure the time filter and visualization work as intended.
# Output of Task-1 :
![Image](https://github.com/user-attachments/assets/80dee014-6af8-401a-a570-76c03894e74e)

# Task- 2
 Generate a heatmap to show the correlation matrix between installs, ratings, and review counts. Filter the data to include only apps that have been updated within the last year and have at least 100,000 installs and reviews count should be more than 1k and genres name should not be Starting with characters A , F , E , G , I , K . this graph should work only between 2 PM IST to 4 PM IST apart from that time we should not show this graph in dashboard itself.
### Libraries used:
pandas,numpy,seaborn,matplotlib,datetime
### Step-By-Step Plan:
##### 1.Import the Required Libraries:
###### ->Import libraries like pandas, numpy, seaborn, matplotlib, and datetime.
##### 2.Filter the Data:
###### ->Filter apps that meet the following conditions:
###### ->Updated within the last year.
###### ->Have at least 100,000 installs.
###### ->Have more than 1,000 reviews.
###### ->Do not belong to genres with names starting with A, F, E, G, I, or K.
##### 3.Calculate Correlation Matrix:
###### ->Select only the required numerical columns (installs, ratings, review counts) from the filtered dataset.
###### ->Compute the correlation matrix using DataFrame.corr().
##### 4.Set Time Restriction:
###### ->Get the current time using datetime.datetime.now() and check if it falls between 2 PM IST and 4 PM IST.
###### ->If outside this time range, do not display the heatmap.
##### 5.Generate and Plot Heatmap:
###### ->If within the allowed time, use Seaborn’s heatmap() to visualize the correlation matrix.
###### ->Customize the heatmap with proper labels, a title, and an aesthetically pleasing color palette.
##### 6.Integrate with Dashboard:
###### ->Implement conditional logic to include or exclude this graph in the dashboard based on the time restriction.
# Output of Task-2 :

# Task-3
Plot a time series line chart to show the trend of total installs over time, segmented by app category. Highlight periods of significant growth by shading the areas under the curve where the increase in installs exceeds 20% month-over-month and content rating should be teen and app name should start with letter ‘E’ and installs should be more than 10k as well as this graph should work only between 6 PM IST to 9 PM IST apart from that time we should not show this graph in dashboard itself.
### Libraries used:
pandas,numpy,seaborn,matplotlib.pylot,datetime,pytz
### Step-By-Step Plan:
##### 1.Import the Required Libraries:
###### ->Import libraries like pandas, numpy, seaborn, matplotlib.pyplot, pytz and datetime.
##### 2. Aggregate Data by Month and Category
###### ->Group the data by month and app category to calculate the total installs for each group.
##### 3. Calculate Month-over-Month Growth
###### ->Compute the month-over-month percentage increase for installs.
##### 4. Define a Function to Plot the Graph
###### ->Implement logic to check if the current time is between 6 PM and 9 PM IST.
##### 5. Call the Function
###### ->Execute the function to display the graph during the specified time window.
##### 6.Integrate with Dashboard:
###### ->Implement conditional logic to include or exclude this graph in the dashboard based on the time restriction.
# Output of Task-3 :

