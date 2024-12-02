# The Samsung Galaxy S23 Price Index

![Samsung](Samsung-Galaxy-S23.png.webp "Samsung")

Source:https://recy-cell.ca/en/products/samsung-galaxy-s23/, retrieved on December 2, 2024.

## Introduction

Nowadays, smartphones have become an essential part of our daily lives, making smartphones a perfect product of choice for a global price comparison index. Among all the different smartphone brands, the Samsung Galaxy stands out as one of the ideal choices for a price index, due to its widespread availability and popularity across the world. With its availability across different regions, it allows us to compare the price of the product from a wide variety of countries, providing meaningful insights into the concept of purchasing power parity.

### 1.

### 2.

### 3.

### 4. Displaying the currencies by currency code

For this step, the method used was doing an online research of the currency code of each country included in the list. The source of the currency codes were from:https://openknowledge.fao.org/server/api/core/bitstreams/7d0c5832-7360-4f49-962d-ccf72338dc79/content, as I went through the document and listed them down by countries. In the code cell, the “currencies: list contains the currency codes corresponding to the countries in order, such as "USD" for the United States, "CAD" for Canada, "GBP" for the United Kingdom, etc. 

Next, I combined the column “currencies” with the table “Cleanedtable”, by using the Cleanedtable.with_column method to create a new table, named “table_with_currencies”, by adding the currencies list as a new column named "Currency" to the existing table, “Cleanedtable”. This shows each country's local price in the table with its respective currency.

Furthermore, in order to make “table_with_currencies” more organized visually, I added an additional code cell and made a new table named “tidied_price_table”, as I moved the column "CAD equivalent '$'" to the last column by using the .move_to_end method. The purpose of this action was to tidy up the table, and make the table seem more organized and in order.

### 5. Calculate difference and plot the differences

Since the CAD equivalent prices were already in the graph from the previous steps, this step would be to calculate the price differences of the product in each country between the price in Canada, using CAD. First, a variable named “price_differences” is calculated by subtracting the value 1099.99 (the price of the product in Canada) from the "CAD equivalent '$'" column of the “tidied_price_table”. This would result in a new array where each entry of the column would show a difference between the prices of our product in each country and the price of the product in Canada. 

I then added a new column named “Difference” to the “tidied_price_table”, and named this new table as “price_table_with_differences”. This table now includes a column with the calculated price difference between each country and Canada itself. Furthermore, since I am only looking for the price difference in each country compared to Canada, I will be excluding the price of the product in Canada, by using the .exclude method. A new table named “FINAL_price_table” is created, which consists of the price differences between each country, excluding Canada.

The last part of this step is to plot the differences between each country. This part was done by simply using the .barh method on the “FINAL_price_table”, on the “Difference” column.

![PD](price_difference.png "pd")

As shown in the graph, you can see that the countries that you’re worst off in buying the Samsung Galaxy S23 are Mexico and Brazil. Furthermore, it can be seen that you could save more than $100 Canadian Dollars by purchasing the model Samsung Galaxy S23 in China. 

### 6. 

### 7.
