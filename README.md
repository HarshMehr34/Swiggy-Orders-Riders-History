# 📌 Project Overview
. This project analyzes the relationship between First-Mile Distance (driver-to-restaurant) and Order Assignment Latency to identify bottlenecks in the delivery dispatch lifecycle. By analyzing thousands of data points for both delivered and cancelled orders, the study aims to optimize driver dispatching logic and reduce order churn.

# 📊 Key Insights & Analytics

### 1. Delivery & Logistics Efficiency
> Distance vs. Time Paradox: Surprisingly, Total Delivery Distance has no significant correlation with Pickup Wait Time or Total Delivery Time. This suggests that external factors like restaurant preparation or traffic density outweigh distance alone.

>  Peak Performance Windows: Delivery performance varies significantly by the day of the week. Fridays and Saturdays see the highest delivery times and assignment latency, while Sundays are the most efficient days for delivery completion.

> Speed & Traffic: Delivery speed peaks during Evening and Morning slots. The Afternoon slot shows a significant dip in speed and a spike in cancellations, likely due to peak traffic congestion and rider fatigue.

### 2. Rider Behavior & Experience
> The "Experience" Factor: Riders with high Lifetime Order Counts receive orders faster (Lower Assignment Latency). However, they also show higher "minimum" delivery times, suggesting they are often entrusted with more complex or longer-distance routes.

> Consistency vs. Speed: Riders who handle a higher volume of "Allotted Orders" work more efficiently across all stages (Assignment, Pickup, and Delivery). Conversely, riders with low allotment counts show higher latencies and a higher probability of eventually churning.

> The Momentum Effect: As a rider's Session Time increases, their Acceptance Rate also increases. This indicates that riders become more "dialed-in" or committed to fulfilling orders as their shift progresses.

### 3. Order Churn & Reassignment
> Cancellation Triggers: The primary drivers for order cancellation are High First-Mile Distance and High Pickup Latency.

> Service Reliability: The system maintains a 98.9% Delivery Success Rate. Late deliveries (defined as >50 mins) account for only 4.5% of the total volume.

> Reassignment Mechanics: 2.5% of orders require reassignment, with the vast majority (97.5%) being fulfilled by the first allotted rider. The most common reason for reassignment is "Rider Inaction," which triggers an Automatic Reassignment flow.

# 🛠 Tech Stack
> Data Manipulation: Python, Pandas, NumPy
> Visualization: Matplotlib, Seaborn (Scatter plots, Pie charts, Bar plots, Line plots)
> Feature Engineering: Feature Creation, Time-delta calculations (Latency in seconds), Time-of-day binning (Morning/Afternoon/Evening), and Experience-based segmenting.


# 💡 Business Recommendations
> Recommendation: Implement Dynamic Geofencing. This keeps riders closer to restaurants, reducing the "Pickup Latency" by reducing first-mile-distance for riders that leads to customer cancellations.

> Recommendation: Prioritize "Power Riders" for complex, high-value order batches. Since they have higher efficiency, they can handle the "long-distance" assignments that would normally cause a newer rider to cancel or delay.

> Recommendation: Introduce a "Shift-Starter Bonus." Since acceptance rates increase as session time increases, we can offer a incentive for completing the first 3 or 4 orders within a certain timeframe to reduce early-session cancellations.

> Recommendation: Reduce the "Auto-Reassignment" timer. If a rider shows no movement toward a restaurant within 120 seconds of acceptance (instead of waiting for "Inaction"), the system should proactively ping the rider or trigger a "Shadow Reassignment" to find a backup.

> Recommendation: Introduce a "Friday Saturday Bonus" to offer a incentive for completing each order delivery so Newer Riders also start taking nearby Order Deliveries leading to higher riders availability and Order Assignment.

# Data Cleaning:
> Dealing with NULL Values: Fixed the Error Data by removing the NULL values, replacing the NULL values with Mode, Median Imputation.
> Dealing With Outliers: Dealt with Outliers using IQR(Inter Quartile Range) Method and Understanding the Skewness the data for using Imputation Techniques.
> Dealing with DataType and Duplicate Values: Understanding the Data and changing the Data Type Accordingly and Removing or keeping the Duplicates accordingly.
