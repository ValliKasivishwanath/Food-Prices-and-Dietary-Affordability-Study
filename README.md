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

**Chart 3: Comparison of Healthy Diet Affordability by Country Relative to World Average**

This dashboard provides a comparative analysis of healthy diet affordability across countries in different continents, relative to the world average. The bar charts are organized by continent, allowing for a quick comparison within and across regions.

**Asia:** Countries like Japan and Bhutan have a higher cost of a healthy diet, with values reaching up to 5.529 units and 4.383 units, respectively, while countries like Israel and Azerbaijan have lower costs, around 2.436 units and 2.348 units, respectively.

**Europe:** A similar variation is observed, with countries like Bosnia and Herzegovina and Albania showing higher costs (3.847 and 3.952 units), compared to Austria and Belgium, which have relatively lower costs.

**North America:** Jamaica stands out with the highest cost at 5.975 units, while Belize and Canada have significantly lower costs at around 2.476 and 2.853 units, respectively.

**South America:** The cost varies, with Guyana and Suriname showing higher costs (4.629 and 4.969 units), compared to Brazil and Ecuador, where the costs are relatively lower.

This dashboard enables users to compare the affordability of a healthy diet by country and continent, providing insights into regional dietary costs relative to the global average.

**Chart 4: Cost Share of Fruits in a Least Cost Healthy Diet -- Pyramid Chart**

This dashboard highlights the cost share of fruits as a percentage of the least expensive healthy diet across various countries, organized by continent. The charts provide a detailed look at how much of the diet cost is attributed to fruits.

The dashboard includes a pyramid chart that visually compares the cost share of fruits across the three continents—Asia, Africa, and Europe. The pyramid chart provides a clear hierarchical view, highlighting the countries with the highest and lowest fruit cost shares.

**Asia:** Malaysia and Pakistan have the highest cost share for fruits, with values reaching 28.80% and 27.10%, respectively, while Tajikistan and Saudi Arabia have the lowest, around 20.70% and 21.50%, respectively.

**Africa:** Tunisia stands out with the highest cost share of fruits at 32.40%, followed by countries like Namibia and Ethiopia, with shares ranging from 24.50% to 25.00%.

**Europe:** The cost share of fruits in a healthy diet is also significant in countries like Luxembourg (30.60%) and Spain (29.50%), while countries like Austria and Ireland have slightly lower shares, around 29.30% and 25.90%, respectively.

This dashboard allows users to explore the proportion of diet costs dedicated to fruits in different countries, offering valuable insights into the economic importance of fruits in a balanced diet.
