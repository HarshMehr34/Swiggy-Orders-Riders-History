# 📌 Project Overview
. This project analyzes the relationship between First-Mile Distance (driver-to-restaurant) and Order Assignment Latency to identify bottlenecks in the delivery dispatch lifecycle. By analyzing thousands of data points for both delivered and cancelled orders, the study aims to optimize driver dispatching logic and reduce order churn.

# 📊 Key Insights & Analytics

### 1. Delivery & Logistics Efficiency
> Distance vs. Time Paradox: Surprisingly, Total Delivery Distance has no significant correlation with Pickup Wait Time or Total Delivery Time. This suggests that external factors like restaurant preparation or traffic density outweigh distance alone.

>  Peak Performance Windows: Delivery performance varies significantly by the day of the week. Fridays and Saturdays see the highest delivery times and assignment latency, while Sundays are the most efficient days for delivery completion.

> Speed & Traffic: Delivery speed peaks during Evening and Morning slots. The Afternoon slot shows a significant dip in speed and a spike in cancellations, likely due to peak traffic congestion and rider fatigue.

### 2. Rider Behavior & Experience
. The "Experience" Factor: Riders with high Lifetime Order Counts receive orders faster (Lower Assignment Latency). However, they also show higher "minimum" delivery times, suggesting they are often entrusted with more complex or longer-distance routes.

. Consistency vs. Speed: Riders who handle a higher volume of "Allotted Orders" work more efficiently across all stages (Assignment, Pickup, and Delivery). Conversely, riders with low allotment counts show higher latencies and a higher probability of eventually churning.

. The Momentum Effect: As a rider's Session Time increases, their Acceptance Rate also increases. This indicates that riders become more "dialed-in" or committed to fulfilling orders as their shift progresses.

### 3. Order Churn & Reassignment
. Cancellation Triggers: The primary drivers for order cancellation are High First-Mile Distance and High Pickup Latency.

. Service Reliability: The system maintains a 98.9% Delivery Success Rate. Late deliveries (defined as >50 mins) account for only 4.5% of the total volume.

. Reassignment Mechanics: 2.5% of orders require reassignment, with the vast majority (97.5%) being fulfilled by the first allotted rider. The most common reason for reassignment is "Rider Inaction," which triggers an Automatic Reassignment flow.

🛠 Tech Stack
Data Manipulation: Python, Pandas, NumPy

Visualization: Matplotlib, Seaborn (Scatter plots, Pie charts, Bar plots, Line plots)

Feature Engineering: Time-delta calculations (Latency in seconds), Time-of-day binning (Morning/Afternoon/Evening), and Experience-based segmenting.
# 🛠 Tech Stack
. Language: Python

. Libraries: Pandas (Data Wrangling), Matplotlib/Seaborn (Visualization), NumPy

. Analysis Techniques: Scatter Plot Density Analysis, Latency Distribution, Geospatial Constraint Identification.

# 📈 Visualizations

💡 Business Recommendations
Dynamic Radius: Implement a dynamic first-mile radius that expands from 4 to 5 units during low-supply periods to capture more orders.

Predictive Re-assignment: Orders not assigned within 120 seconds should be flagged for "Priority Dispatch" to prevent them from entering the high-latency churn zone.


# Data Cleaning:
. Add a small section in your README or Notebook about how you handled outliers or null values. In real-world data jobs, cleaning is 80% of the work.
