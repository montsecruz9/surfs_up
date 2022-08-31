# Surfs_Up
## Overview of the Project
An analysis was made to get information about the temperature in Oahu, Hawaii. This, with the purpose of choosing the right location to open a surf and ice cream shop. This project gathered temperature information for the months of June and December, in order to determine if the business is sustainable year-round.

## Results
- This is the dataframe from the list of temperatures for the month of June. 

![image](https://user-images.githubusercontent.com/104812189/187568076-be264312-598e-4c32-a557-8f267a5279db.png)

- The following statistics were calculated from this dataframe:

![image](https://user-images.githubusercontent.com/104812189/187570382-991e9bec-fd28-472e-9ce0-e14ed33e1026.png)

- This is the dataframe from the list of temperatures for the month of December.

![image](https://user-images.githubusercontent.com/104812189/187570636-e6aeb72d-3e31-4127-ac5c-0a1bb0ac2394.png)

- The following statistics were calculated from this dataframe:

![image](https://user-images.githubusercontent.com/104812189/187570705-4ab5f32f-7cd9-4e41-91b4-d60e56fa5354.png)

Three key differences between June and December's data
1. The minimum temperature for June is 64°F and for December is 56°F.
2. The maximum temperature for June is 85°F and for December is 83°F.
3. The mean temperature for June is 74.94°F and for December is 71.04°F

## Summary
By looking at the statistics from this data, we can conclude that temperatures around the year doesn't vary that much. December might have lower temperatures but, overall, has a mean temperature of 71.04°F with a standard deviation of 3.75. June has a mean temperature of 74.94°F with a standard deviation of 3.26. 
This means the surf and ice cream shop business is sustainable the whole year.
However, we can gather even more weather data. We can analyze precipitation trends during the same months, to have an idea of how much it rains during the year. 
We can try this out: 
- Query for precipitation in June:
june_rain = session.query(Measurement).filter(extract('month', Measurement.date) == 6)

- Query for precipitation in December:
dec_rain = session.query(Measurement).filter(extract('month', Measurement.date) == 12)

Then, for both queries, convert the data into a list, create a dataframe and then get the statistics, just as we did for the temperatures. 

June
![image](https://user-images.githubusercontent.com/104812189/187587368-13229ea9-6105-4803-b1bc-434734c5a98b.png)

December
![image](https://user-images.githubusercontent.com/104812189/187587468-c4bc6f54-50d5-43f2-bfd1-fbd8d9470eda.png)

