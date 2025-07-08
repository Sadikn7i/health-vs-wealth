Health vs Wealth: Predicting GNI from Life Expectancy using Random Forest
This project explores the connection between national health outcomes and economic prosperity by using a Random Forest regression model to predict Gross National Income (GNI) per capita from life expectancy data. It focuses on how well a single health indicator—life expectancy can explain variations in income across countries.

***Key Insights
The model confirms a strong and measurable link between health and wealth, particularly for low to middle-income countries. On the left side of the prediction plot, where actual GNI is below approximately $40,000, the predicted values closely follow the perfect prediction line. This tight clustering indicates that the model performs exceptionally well for countries within this income bracket.

However, the model's prediction accuracy declines as GNI increases. For high-income nations, the error margins grow significantly, a phenomenon known as heteroscedasticity. This arises due to omitted-variable bias—life expectancy alone is not sufficient to account for wealth at higher levels of economic development. Other unaccounted-for variables like technological advancement, natural resource wealth, and institutional quality begin to dominate in wealthier countries.

For example, on the right side of the plot, representing high-income countries, the prediction points are scattered and deviate significantly from the perfect prediction line. This shows that the model tends to underperform when dealing with the economic complexities of richer nations.

***Example Prediction
The model was used to predict the GNI of a hypothetical country with a life expectancy of 75 years. It returned a predicted GNI of approximately $9,398.30.

This prediction is both statistically meaningful and realistic. The average life expectancy in the dataset was around 73, with the 75th percentile near 78. Choosing a value of 75 ensures we are making a prediction in a range where the model has seen ample training data and is known to perform well.

The specific number chosen is not critical; it simply demonstrates the process of using the model to predict outcomes for new data.

***Model Behavior
The model was trained using only one feature: Life Expectancy. As expected, the feature importance score for this variable is 1.0, meaning it accounts for 100% of the model’s decision-making. This makes the model simple, interpretable, and ideal for highlighting the predictive power of health metrics alone.

Additionally, a visualization of a single decision tree from the Random Forest helps illustrate how the model breaks down predictions into simple logical steps. For a country with a life expectancy of 75 years, the model follows a clear path through the tree based on threshold splits until it reaches a predicted GNI value. The final output is the average result from all trees in the forest.

***Data Sources and Acknowledgments
The data used in this analysis comes from the World Development Indicators (WDI) database provided by the World Bank. The data was accessed programmatically via the official World Bank API.

Primary Source: The World Bank – World Development Indicators (WDI)

Indicators Used:

GNI per capita, Atlas method (current US$): NY.GNP.PCAP.CD

Life expectancy at birth, total (years): SP.DYN.LE00.IN

We acknowledge the World Bank for providing open access to this valuable dataset, which enables research into global development trends.


