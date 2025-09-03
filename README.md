# Forecasted-social-media-category-trends-using-KPIs-and-AI-driven-time-series-modeling.

## 📌 Project Summary (GitHub README)

### **Social Media Engagement Trend Analysis & Forecasting**

This project performs an **end-to-end pipeline** for analyzing and forecasting **social media engagement trends** across multiple categories using **synthetically generated data**.

#### 🔹 Data Generation

* The dataset was **randomly generated** using Python libraries (`numpy`, `pandas`) to simulate realistic social media interactions.
* Categories such as *Technology, Health, Entertainment, Finance, etc.* were predefined.
* Engagement metrics (**likes, dislikes, comments**) were generated using random integer distributions:

  * Likes: `np.random.randint(0, 10000)`
  * Dislikes: `np.random.randint(0, 5000)`
  * Comments: `np.random.randint(0, 3000)`
* This ensures variability and randomness while maintaining **statistical realism** for testing models.

#### 🔹 Key Performance Indicators (KPIs)

The following KPIs were computed per category to assess performance:

1. **Engagement Rate (ER)** → % share of total interactions.
2. **Like-to-Comment Ratio (LCR)** → Indicator of passive vs. active engagement.
3. **Comment Rate (CR)** → Proportion of comments among total interactions.
4. **Like-to-Dislike Ratio (LDR)** → Audience approval ratio.
5. **Sentiment Score (SS)** → Normalized metric of audience sentiment.
6. **Category Popularity Index (CPI)** → Share of category in overall engagement.
7. **Engagement Depth (CED)** → Discussion depth (comments vs. reactions).
8. **Virality Score (VS)** → Speed of reactions vs. depth of conversation.
9. **Approval Engagement Score (AES)** → Balance of likes vs. comments.

#### 🔹 Analytical Insights

* Identified **categories losing trendiness** based on declining monthly interactions.
* Highlighted **current trending categories** by analyzing the last 30-day interaction volume.
* Derived **category performance rankings** based on KPI scores.

#### 🔹 Forecasting Approach

* Applied **time-series forecasting** to predict category-level engagement trends.
* Traditional methods such as **Holt-Winters Exponential Smoothing** were tested but showed convergence issues due to data noise.
* Switched to **Prophet (AI-driven forecasting)** for improved robustness:

  * Automatically captures **trend, seasonality, and noise**.
  * Provides **3-month ahead predictions with confidence intervals**.
  * Outputs indicate which category has the **highest probability of becoming the next trend**.

#### 🔹 Applications

* **Marketing Strategy** → Focus on categories with rising forecasted engagement.
* **Content Planning** → Reduce investment in declining categories.
* **Community Engagement** → Prioritize categories with higher comment depth.
* **Reputation Monitoring** → Track sentiment scores for early detection of negative trends.
