# Keshav_google-play-store-review-analytics
NULL CLASS INTERNSHIP PROJECT
# Task- 1 and 2 code

#import pandas as pd
#import plotly.express as px
#from datetime import datetime
#import pytz

Load your dataset

Replace 'your_dataset.csv' with the actual dataset file path

#data = merged_df

Filter 1: Exclude categories starting with "A," "C," "G," or "S"

#filtered_data = data[~data['Category'].str.startswith(('A', 'C', 'G', 'S'))]

Filter 2: Top 5 categories by total installs

top_categories = (
    filtered_data.groupby('Category')['Installs']
    .sum()
    .nlargest(5)
    .index
)
#filtered_data['Highlight'] = filtered_data['Installs'] > 1_000_000
#filtered_data.head()
Time-based check
#ist = pytz.timezone('Asia/Kolkata')
#current_time = datetime.now(ist).time()

Allowed time range (6 PM to 8 PM IST)
#start_time = datetime.strptime("18:00:00", "%H:%M:%S").time()
#end_time = datetime.strptime("20:00:00", "%H:%M:%S").time()

#if start_time <= current_time <= end_time:
    Create Choropleth map
    #fig = px.choropleth(
        filtered_data,
        color="Category",
        hover_name="Category",
        hover_data={"Installs": True,"Category": True},
        title="Global Installs by Top App Categories (Filtered)",
        color_continuous_scale=["lightgray", "red"],
    )

    fig.show()
#else:
    print("The Choropleth map can only be viewed between 6 PM and 8 PM IST.")


# Task - 3 code

import pandas as pd
import plotly.graph_objects as go
from datetime import datetime
import pytz

Assuming aggr_data['month'] is in string format, convert it to datetime if needed
#aggr_data['month'] = pd.to_datetime(aggr_data['month'], format='%Y-%m')  # adjust the format if necessary

Time-based check (6 PM to 9 PM IST)
#ist = pytz.timezone('Asia/Kolkata')
#current_time = datetime.now(ist)

#if current_time.hour >= 18 and current_time.hour < 21:
    Create a Plotly line chart
    #fig = go.Figure()

    # Add data for each category
    for category in aggr_data['Category'].unique():
        category_data = aggr_data[aggr_data['Category'] == category]
        fig.add_trace(go.Scatter(
            x=category_data['month'],
            y=category_data['Installs'],
            mode='lines+markers',
            name=category,
            line=dict(shape='linear'),
            marker=dict(symbol='square')
        ))

        # Highlight significant growth areas (greater than 20%)
        significant_growth = category_data[category_data['MoM Growth'] > 20]
        fig.add_trace(go.Scatter(
            x=significant_growth['month'],
            y=significant_growth['Installs'],
            mode='markers',
            name=f"Significant Growth: {category}",
            marker=dict(color='orange', size=10, opacity=0.6)
        ))

    # Update layout
    fig.update_layout(
        title="Trend of Total Installs Over Time (Segmented by Category)",
        xaxis_title="Month",
        yaxis_title="Total Installs",
        legend_title="App Category",
        xaxis=dict(
            tickformat='%b %Y',  # Format x-axis to show Month-Year
            tickangle=45,
            type='date'  # Ensure that Plotly interprets this as a time series
        ),
        template="plotly_dark"
    )

    # Show the plot
    fig.show()

    # Save the Plotly figure as an HTML file
    fig.write_html("time_series_line_chart.html")

else:
    print("This chart is only viewable between 6 PM and 9 PM IST.")
