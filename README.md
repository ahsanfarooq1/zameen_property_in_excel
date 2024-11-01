# Zameen.com Property Dataset Analysis in Excel

## Introduction
This project analyzes a dataset from Zameen.com, Pakistan's premier real estate portal. The dataset contains detailed information about property listings, including property type, price, location, and other characteristics. This analysis aims to extract meaningful insights from the data using various Excel functions.

## Dataset
The dataset used for this analysis is available [here](https://github.com/ahsanfarooq1/zameen_property_in_excel/blob/main/Zameen__Property_Dataset.xlsx).


## Data Description
The dataset comprises 168,428 records and contains the following columns:
1. `property_id`: Unique identifier for each property.
2. `location_id`: Identifier for the location.
3. `property_type`: Type of property (e.g., Flat, House).
4. `price`: Listing price.
5. `location`: Specific area or sector.
6. `city`: City of listing.
7. `province_name`: Province of listing.
8. `latitude`, `longitude`: Geographical coordinates.
9. `baths`: Number of bathrooms.
10. `area`: Combined size and unit of the property.
11. `purpose`: Purpose of the listing (e.g., For Sale).
12. `bedrooms`: Number of bedrooms.
13. `date_added`: Listing date.
14. `Area Type`, `Area Size`, `Area Category`: Area measurements.

## Analysis Questions(KPIs)
Here are some key questions addressed in this analysis:
1. **Count of House Property Types**
2. **Range of Prices for Rent Properties in Islamabad**
3. **Different Property Types Available**
4. **Properties with More Than 3 Bedrooms**
5. **Farm Houses Added in 2019**
6. **Flats for Sale with 2 Bathrooms in Faisalabad**
7. **High_Price_Multi_Bed Indicator**
8. **Luxury_Property Indicator**
9. **Recent_High_Value Indicator**
10. **Maximum Area for Farm Houses**
11. **Location of the Most Expensive Property**
12. **Properties for Sale on 7th Avenue, Islamabad**

## Analysis Questions and Answers

1. **Count of House Property Types**  
   - **Answer**: The dataset contains **7 types of properties** with a total of 168,427 listings. **Houses** are the most common property type with **105,453 listings**
   - **Method**: Used Excel `COUNTIF` function on `property_type` column to count entries labeled as "House."

2. **Range of Prices for Rent Properties in Islamabad**  
   - **Answer**: The price range for rent properties in Islamabad is **PKR 1000 to PKR 95,00,000**
   - **Method**: Used `MINIFS` and `MAXIFS` functions on `price` column with conditions `purpose = Rent` and `city = Islamabad`.

3. **Different Types of Properties Listed**  
   - **Answer**: There are **7** unique property types. 
   - **Method**: Used `UNIQUE` function to find distinct values in `property_type` column and `COUNTA` to count them.

4. **Count of Properties with More Than 3 Bedrooms**  
   - **Answer**: There are **64,689** properties with more than three bedrooms.
   - **Method**: Used `COUNTIF` on `bedrooms` column to find entries with bedrooms > 3.

5. **Farm House Properties Added in 2019**  
   - **Answer**: **601 Farm House** properties were added in the year 2019
   - **Method**: Used `COUNTIFS` with conditions for `property_type = Farm House` and `date_added` in the year 2019.

6. **Flats for Sale with 2 Bathrooms in Faisalabad**  
   - **Answer**: **only 1 flat** is available for sale with exactly two bathrooms in Faisalabad
   - **Method**: Used `COUNTIFS` with conditions on `property_type = Flat`, `baths = 2`, `purpose = For Sale`, and `city = Faisalabad`.

7. **High_Price_Multi_Bed Indicator**  
   - **Answer**: Created a column named `High_Price_Multi_Bed` where properties with more than 3 bedrooms and a price above 10,000,000 are marked.
   - **Method**: Used conditional formattting to highlight entries that meet both conditions.

8. **Luxury_Property Indicator**  
   - **Answer**: Created a column named `Luxury_Property` for properties in Islamabad or Lahore with more than 4 bedrooms and bathrooms.
   - **Method**: Used conditional formatting in specified cities with the required attributes.

9. **Recent_High_Value Indicator**  
   - **Answer**: Created a column named `Recent_High_Value` for properties listed in 2023 with a price above 15,000,000.
   - **Method**: Used conditional formatting to identify recent high-value properties.

10. **Maximum Area of Farmhouse Properties**  
    - **Answer**: The maximum area of a farmhouse property is **416 kanal**
    - **Method**: Used `MAXIFS` on `area` column for properties where `property_type = Farm House`.

11. **Location of the Most Expensive Property**  
    - **Answer**: The most expensive property is located in **Karachi, Sindh**
    - **Method**: Used `INDEX/MATCH` with `MAX` on `price` column to identify location.

12. **Properties for Sale in 7th Avenue, Islamabad**  
    - **Answer**: There are **5 properties** for sale on 7th Avenue, Islamabad
    - **Method**: Used `COUNTIFS` with conditions `location = 7th Avenue` and `city = Islamabad`.

## Conclusion
This dataset from Zameen.com provides valuable insights into property trends across Pakistan, with data-driven answers to commonly asked questions. The analysis revealed key metrics such as the prevalence of certain property types, city-wise price ranges, and criteria for luxury properties, which can help in understanding market dynamics for various property categories.









