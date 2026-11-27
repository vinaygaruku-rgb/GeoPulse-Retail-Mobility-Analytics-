
# GeoPulse Data Dictionary

## 1. Overview
This document describes the fields, data types and expected values used in the GeoPulse retail mobility dataset.

Each record represents an aggregated observation for a retail location during a particular hour.

## 2. Dataset Fields

| Column Name | Data Type | Description |
|---|---|---|
| date | Date | Date of observation |
| time | Time | Hour of observation |
| location_id | String | Unique identifier for a retail location |
| location_name | String | Name of the retail area |
| latitude | Float | Geographic latitude of the location |
| longitude | Float | Geographic longitude of the location |
| footfall | Integer | Number of visitors recorded during the hour |
| store_category | String | Category of retail activity |
| transactions | Integer | Number of purchases during the hour |
| revenue | Float | Total revenue generated during the hour in INR |
| weather | String | Weather condition during observation |

## 3. Expected Values

### date
Format: YYYY-MM-DD

### time
Format: HH:MM (24-hour format)

### location_id
Example: LOC001, LOC002

### location_name
Example: Shopping Street, Market Area, City Centre

### latitude
Geographic coordinate in decimal degrees.

### longitude
Geographic coordinate in decimal degrees.

### footfall
Non-negative integer representing aggregated visitor counts.

### store_category
Examples:
- Grocery
- Clothing
- Electronics
- Food and Beverage
- Pharmacy
- General Retail

### transactions
Non-negative integer representing completed purchases.

### revenue
Non-negative numeric value measured in Indian Rupees (INR).

### weather
Examples:
- Sunny
- Cloudy
- Rainy
- Windy

## 4. Data Quality Rules

- Date and time must follow consistent formats.
- Location IDs must not be missing.
- Latitude must be between -90 and 90.
- Longitude must be between -180 and 180.
- Footfall and transactions cannot be negative.
- Revenue cannot be negative.
- Duplicate observation records must be investigated.
- Missing values must be identified and documented.

## 5. Notes

The dataset will initially contain synthetic data generated using Python.

Footfall represents aggregated visitor counts, not identified or individually tracked customers.

Revenue and transaction values are simulated for project analysis and do not represent actual business performance.
