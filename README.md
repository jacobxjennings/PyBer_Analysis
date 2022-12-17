# PyBer_Analysis

## Overview
In this analysis we review customer and driver datasets provider by the app PyBer. Our goal is to summarize to management how much money drivers are earning in different city types such as: Urban, Suburban, and Rural. We used multiple datasets to create our summary and also extracted date of total rides, drivers, fares, and average fare type and total fares by city type. 

## Total Rides
From our dataframe, we first counted all unique ride IDs and grouped by the city type as described above. This provided us with 1625 urban rides, 625 suburban rides, and 125 rural rides. 

    rides_per_city_type = pyber_data_df.groupby('type').count().ride_id
    rides_per_city_type

## Total Drivers
To fine the total number of total drivers, grouped by city type, we combined driver_count of the city_data_df and drive_count. There are 2405 urban drivers, 490 suburban drivers, and 78 rural drivers.

    total_drivers_per_city_type = city_data_df.groupby('type').sum().driver_count
	total_drivers_per_city_type

## Total Fares
By summing fare from pyber_data_df and grouping by the city type, we calculate that urban area earned $39,854, suburban areas earned $19,356, and rural area earned $4,327. 

    total_fares = pyber_data_df.groupby('type').sum().fare
	total_fares

## Total Fare by City Type
To calculate the total fare by city type, we extract the total amount of all fares per city types. Urban areas bring in $39,854, suburan areas bring in $19,356, and rural areas bring in $4327. 

    total_fares = pyber_data_df.groupby('type').sum().fare
    total_fares

## Summary
![PyBer Ride-Sharing Data (2019)](https://github.com/jacobxjennings/PyBer_Analysis/blob/main/PyBer_fare_summary.png?raw=true)
