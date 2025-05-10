# Airline Customer Data Analysis

## About
This project performs an unsupervised analysis of airline customer data to segment passengers and identify key satisfaction drivers. Using techniques like PCA, MCA, CAH, and k-means, it uncovers actionable insights to enhance customer experience and loyalty.

## Objectives
1. **Segment Customers**: Group passengers into homogeneous clusters based on socio-demographics, travel habits, and satisfaction levels.
2. **Identify Satisfaction Drivers**: Analyze variables impacting customer experience, such as in-flight Wi-Fi, seat comfort, and delay management.
3. **Provide Actionable Insights**: Offer strategic recommendations to improve service quality and customer retention.

## Dataset
- **Source**: Modified Kaggle dataset from John D., based on a passenger satisfaction survey.
- **Dimensions**: 500 passengers × 24 variables.
- **Variables**:
  - **Qualitative**: Gender, Customer Type (Loyal/Disloyal), Type of Travel (Business/Personal), Class (Business/Eco/Eco Plus).
  - **Quantitative**: Age (7-85 years), Flight Distance (31-4983 miles), 14 service satisfaction scores (0-5), Departure/Arrival Delays (0-1592 minutes).
- **Preprocessing**:
  - Removed irrelevant columns (`Unnamed: 0`, `Id`).
  - Handled missing values in `Arrival Delay in Minutes` by imputing the median (0).

## Methodology
1. **Principal Component Analysis (PCA)**:
   - Reduced dimensionality of 18 quantitative variables.
   - Visualized correlations between service satisfaction scores.
2. **Hierarchical Ascendant Classification (CAH) & k-means**:
   - Segmented customers into clusters, with k-means selecting 3 clusters based on the elbow method.
3. **Multiple Correspondence Analysis (MCA)**:
   - Explored relationships between qualitative variables (e.g., Type of Travel and Class).
4. **Visualization**:
   - Histograms, boxplots, scatterplots, and dendrograms to interpret distributions and cluster structures.

## Key Findings
- **Customer Segments**:
  - **Cluster 1**: Business travelers, often in Business Class, highly satisfied with services, sensitive to Wi-Fi and booking ease.
  - **Cluster 2**: Personal travelers, mostly in Eco Class, less satisfied, particularly with seat comfort and delays.
  - **Cluster 3**: Mixed group, moderate satisfaction, varied travel purposes.
- **Satisfaction Drivers**:
  - In-flight service and baggage handling are strengths (mean scores ~3.65/5).
  - Wi-Fi (2.72/5) and online booking (2.76/5) show polarized feedback, indicating improvement potential.
  - Delays, though rare, significantly impact satisfaction when they occur.
- **Qualitative Insights**:
  - Business travelers in Business Class prioritize Wi-Fi and booking ease.
  - Personal travelers in Eco Class are more sensitive to seat comfort and check-in experience.

## Installation
1. **Prerequisites**:
   - Python 3.8+
   - Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `tabulate`
2. **Setup**:
   - Clone the repository: `git clone https://github.com/yourusername/airline-customer-analysis.git`
3. **Run**:
   - Open `Compagnie_aérienne.ipynb` in Jupyter Notebook or Google Colab.
   - Ensure the dataset (`airline_customer_satisfaction.csv`) is in the project directory.

## Project Structure
- `Compagnie_aérienne.ipynb`: Main notebook with data analysis, visualizations, and clustering.
- `airline_customer_satisfaction.csv`: Dataset file.
- `requirements.txt`: List of required Python libraries.
- `figures/`: Directory for generated plots (e.g., histograms, boxplots, scatterplots).

## Usage
1. Load the dataset and run preprocessing steps to clean data.
2. Execute exploratory data analysis (univariate and bivariate) to understand variable distributions.
3. Perform PCA and MCA to reduce dimensionality and explore variable relationships.
4. Apply CAH and k-means for clustering, visualizing results with scatterplots.
5. Review strategic recommendations based on cluster profiles and satisfaction insights.

## Recommendations
1. **Enhance Wi-Fi and Booking**:
   - Upgrade in-flight Wi-Fi reliability, especially for Business Class passengers.
   - Simplify the online booking process to reduce user friction.
2. **Improve Eco Class Experience**:
   - Enhance seat comfort in Economy through better cushioning or spacing.
   - Streamline check-in processes at high-traffic airports.
3. **Minimize Delays**:
   - Implement proactive delay management (e.g., real-time updates, priority rebooking).
4. **Personalize Services**:
   - Offer tailored perks for loyal customers (e.g., lounge access, priority boarding).
   - Customize offers for business vs. personal travelers based on preferences.

## Limitations
- **Dataset Size**: Limited to 500 passengers, potentially missing broader trends.
- **Missing Backend**: No real-time data integration for ongoing analysis.
- **Scope**: Focuses on unsupervised methods, excluding predictive modeling.
- **Qualitative Depth**: Limited depth in qualitative variables due to dataset constraints.

## Future Improvements
- Integrate real-time data via API for dynamic insights.
- Expand dataset with more passengers and variables (e.g., loyalty program data).
- Incorporate supervised learning to predict satisfaction scores.
- Develop a dashboard for interactive visualization of clusters and trends.
- Explore cross-platform deployment (e.g., web app) for stakeholder access.

## Contributors
- **Mahdi TOUMI**

## Acknowledgments
This project was developed as part of a data science course, leveraging a modified Kaggle dataset. Special thanks to John D. for the original dataset and to the open-source community for tools like `scikit-learn` and `seaborn`.
