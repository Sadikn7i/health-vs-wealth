Health vs Wealth: Predicting GNI from Life Expectancy Using Random Forest
This project explores the connection between national health outcomes and economic prosperity by using a Random Forest regression model to predict Gross National Income (GNI) per capita from life expectancy data. It focuses on how well a single health indicator—life expectancy—can explain variations in income across countries.

📌 Key Insights
The model confirms a strong and measurable link between health and wealth, particularly for low to middle-income countries.

On the left side of the prediction plot (where actual GNI is below ~$40,000), the predicted values closely follow the perfect prediction line.

This tight clustering indicates the model performs exceptionally well for countries in this income bracket.

However, the model’s accuracy declines as GNI increases:

For high-income nations, the error margins grow significantly—a pattern known as heteroscedasticity.

This is caused by omitted-variable bias: life expectancy alone is not sufficient to explain income in wealthier countries.

Other influential factors like technology, institutional strength, and natural resources become dominant at higher income levels.

For example, on the right side of the plot, representing rich countries, the prediction points are scattered and deviate noticeably from the perfect prediction line. This clearly shows that the model underperforms in capturing the economic complexity of high-income nations.

🔮 Example Prediction
The model was used to predict the GNI of a hypothetical country with a life expectancy of 75 years.

The predicted GNI was approximately $9,398.30.

This result is both statistically meaningful and realistic:

The average life expectancy in the dataset was about 73.

The 75th percentile was around 78.

Choosing a value of 75 means the model is operating in a zone where it has seen plenty of data and tends to be more accurate.

The exact number is not critical. The goal here is to demonstrate the model’s practical usage on new, unseen data.

⚙️ Model Behavior
The model was trained using only one input feature: Life Expectancy.

The feature importance score is 1.0, confirming that 100% of the model's decision-making is based on life expectancy alone.

This makes the model simple and interpretable, ideal for demonstrating how health correlates with income on a global scale.

A visualization of one decision tree in the Random Forest shows how the model splits the data into logical paths. For instance:

A country with a life expectancy of 75 might follow a path like:

Is 75 ≤ 79.8? → Yes

Is 75 ≤ 72.8? → No

Is 75 ≤ 78.1? → Yes

→ Prediction Reached

The final GNI estimate is the average of all trees in the forest.

📚 Data Sources and Acknowledgments
The data used in this analysis comes from the World Development Indicators (WDI) database, provided by The World Bank.

We accessed the dataset programmatically via the official World Bank API.

🏛 Primary Source:
The World Bank – World Development Indicators (WDI)

📈 Indicators Used:
GNI per capita, Atlas method (current US$)
→ NY.GNP.PCAP.CD

Life expectancy at birth, total (years)
→ SP.DYN.LE00.IN

We gratefully acknowledge the World Bank for providing open access to this valuable dataset, which supports research and policy-making related to global development.
