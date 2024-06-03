# Food-Prices-and-Dietary-Affordability-Study

**DATASET**

The dataset provides comprehensive information on the cost and affordability of various types of diets across different countries, with detailed examples from Albania. It includes metrics such as the cost of an energy-sufficient diet (CoCA), a nutrient-adequate diet (CoNA), and a healthy diet (CoHD). The dataset highlights the economic challenges faced by populations in affording a healthy diet, showing the percentage of people unable to afford these diets. For instance, in Albania, 31.3% of the population cannot afford a healthy diet, affecting approximately 0.9 million people. Additionally, it shows the cost ratio of healthy diets compared to energy-sufficient diets from starchy staples, providing insights into dietary economics. Population data is also included, which helps in understanding the scale of the affordability issue. Overall, the dataset serves as a valuable resource for analyzing food affordability and nutrition security on a global scale.


**Chart 1: The Proportion of the Cost of Each Food Item in Relation to a Healthy Diet**

The bar chart shows the cost of a healthy diet across different continents, with North America being the most expensive at 5.975 units.The pie chart illustrates the proportion of various food items contributing to the cost.Animal-source foods account for the highest proportion at 28.57%.Vegetables and fruits follow, with 24.53% and 17.38%, respectively.Starchy staples and legumes/nuts/seeds make up 16.00% and 8.41% of the cost.Oils and fats are the least significant, contributing only 4.49%.

This dashboard is interactive, allowing users to click on a continent in the bar chart, which dynamically updates the pie chart to reflect the food cost proportions specific to that continent.

**Chart 2: Percentage of Unaffordability of a Healthy Diet - Dendrogram Chart**
This dendrogram chart shows the percentage of the population unable to afford a healthy diet in various Asian countries.Pakistan has the highest unaffordability rate at 81.00%, followed closely by Nepal at 80.40%. India, Bangladesh, and Indonesia also have high rates, above 70%. Countries like Bhutan, Tajikistan, and Armenia show moderate rates ranging from 37.10% to 51.20%. The chart illustrates a decreasing trend in unaffordability towards countries like Japan and Cyprus, with rates below 3%. The color gradient from red to green helps visualize the severity of unaffordability across these nations.

This dashboard is interactive, allowing users to change the continent selection, which dynamically updates the dendrogram chart to reflect the unaffordability rates specific to the selected continent.

**How I Created the Dendrogram Chart:**

**Path Initialization:**
Started by creating the initial path with coordinates (0, 200).
Defined the path bin size as 1 to ensure precise segmentation of the data points.

**Key Calculations**

**Unaffordability Metric:** The metric "Percent of the population who cannot afford a healthy diet (CoHD headcount)/100" is used to indicate the proportion of individuals in a population who cannot afford a healthy diet.

**Window Sum Calculation**: The formula "WINDOW_SUM(sum([Percent of the population who cannot afford a healthy diet (CoHD headcount)]))/2" calculates the cumulative sum of the unaffordability percentage, averaged over a specified window. This helps analyze trends and patterns in food affordability across different time periods or regions.

**Ranking Calculation:** The formula "RANK_UNIQUE([Total Perc],'asc')" assigns a unique rank to each country based on the total percentage of the population who cannot afford a healthy diet, in ascending order. This ensures no two countries share the same rank, even if their unaffordability percentages are identical.

**Calculated X and Y Coordinates:**

Generated the X coordinates based on the **rank** of the countries by their unaffordability percentage.
Computed the Y coordinates using the actual unaffordability percentage values.

**Sigmoid Function Application:**

Created a calculated field for the sigmoid function to smoothen transitions between data points.
Applied the sigmoid function to the Y coordinates for a gradual and visually appealing curve.
Dendrogram Construction:

**Plotted** the X and Y coordinates to form the branches of the dendrogram.
Adjusted aesthetics such as color gradients, ensuring a transition from red (high unaffordability) to green (low unaffordability).

**Interactivity Implementation:**
Set up filters allowing users to select different continents, dynamically updating the dendrogram chart based on the selected data.


