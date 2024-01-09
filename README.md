# Delhivery Data Intelligence

## Business Problem

Delhivery aims to understand and process data from its data engineering pipelines. The key objectives include cleaning, sanitizing, and manipulating data to derive useful features from raw fields. Additionally, the goal is to make sense of the raw data and assist the data science team in building forecasting models.

## Approach

### Basic Data Cleaning and Exploration

1. **Handling Missing Values:**
   - Identified and addressed missing values in the dataset.
2. **Data Structure Analysis:**
   - Explored the structure of the data to gain insights into its characteristics.
3. **Feature Extraction:**
   - Extracted features from fields like Destination Name, Source Name, and Trip_creation_time.

### In-Depth Analysis and Feature Engineering

1. **Time Calculation:**
   - Calculated the time taken between od_start_time and od_end_time as a feature.
2. **Hypothesis Testing:**
   - Conducted hypothesis testing and visual analysis between various aggregated values.

### Outlier Handling and Normalization

1. **Outlier Detection:**
   - Identified outliers in numerical variables.
2. **Outlier Treatment:**
   - Handled outliers using the IQR method.
3. **Data Transformation:**
   - Performed one-hot encoding for categorical variables.
   - Normalized/Standardized numerical features using MinMaxScaler or StandardScaler.

## Problems Encountered and Solutions

1. **Assumption Check:**
   - Addressed non-normality through non-parametric tests and transformations.
2. **Data Quality:**
   - Handled outliers using the IQR method to ensure data integrity.

## Column Profiling

1. **data:**
   - Indicates whether the data is testing or training data.
2. **trip_creation_time:**
   - Timestamp of trip creation.
3. **route_schedule_uuid:**
   - Unique Id for a particular route schedule.
4. **route_type:**
   - Transportation type (FTL, Carting).
5. **trip_uuid:**
   - Unique ID given to a particular trip.
6. **source_center:**
   - Source ID of trip origin.
7. **source_name:**
   - Source Name of trip origin.
8. **destination_center:**
   - Destination ID.
9. **destination_name:**
   - Destination Name.
10. **od_start_time:**
    - Trip start time.
11. **od_end_time:**
    - Trip end time.
12. **start_scan_to_end_scan:**
    - Time taken to deliver from source to destination.
13. **is_cutoff, cutoff_factor, cutoff_timestamp:**
    - Unknown fields.
14. **actual_distance_to_destination:**
    - Distance in Kms between source and destination warehouse.
15. **actual_time:**
    - Actual time taken to complete the delivery (Cumulative).
16. **osrm_time:**
    - Open-source routing engine time calculator (Cumulative).
17. **osrm_distance:**
    - Open-source routing engine distance calculator (Cumulative).
18. **factor:**
    - Unknown field.
19. **segment_actual_time:**
    - Segment time - Time taken by the subset of the package delivery.
20. **segment_osrm_time:**
    - OSRM segment time - Time taken by the subset of the package delivery.
21. **segment_osrm_distance:**
    - OSRM distance - Distance covered by the subset of the package delivery.
22. **segment_factor:**
    - Unknown field.

## Observations from the Results

1. **Temporal Patterns:**
   - Noted hourly and monthly trends in trip creation.
   - Identified popular weeks for trip creation.
   - Analyzed mid-month preference for trip creation.
2. **Geographical Patterns:**
   - Explored trip distribution across states and cities.
   - Identified top cities for trip origination and termination.
3. **Feature Analysis:**
   - Found statistically similar features and differences.
   - Discovered high correlation among numerical columns.

## Recommendations

1. **Routing System Enhancement:**
   - Improve the OSRM trip planning system to address discrepancies.
   - Reduce the difference between osrm_time and actual_time for better delivery time predictions.
2. **Geographic Expansion:**
   - Enhance existing corridors to improve penetration in high-demand states.
   - Conduct customer profiling in key states for a better understanding of customer behavior.
3. **Traffic and Terrain Considerations:**
   - Analyze heavy traffic and terrain conditions in specific states for better planning during peak seasons.

## Conclusion

The analysis provides valuable insights into data patterns, anomalies, and areas for improvement. By implementing the recommendations, Delhivery can optimize its routing system, expand strategically, and enhance the overall customer experience.
