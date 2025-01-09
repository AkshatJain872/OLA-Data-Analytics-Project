# OLA Data Analytics Project Documentation

## Project Title: OLA Data Analytics Dashboard (SQL & Power BI)

### **Project Overview**
This project focuses on analyzing ride data from OLA using SQL for data processing and creating an interactive dashboard in Power BI. The dashboard provides key insights into ride patterns, revenue trends, customer segmentation, and more, helping to improve business decision-making.

### **Objective**
- To analyze OLA ride data to uncover meaningful patterns and insights.
- To automate data processing using SQL queries.
- To create a Power BI dashboard for real-time data visualization.

### **Tools and Technologies Used**
- **SQL**: For data extraction, cleaning, transformation, and analysis.
- **Power BI**: For creating an interactive dashboard to visualize key metrics.
- **Excel/CSV Files**: For initial data storage.

### **Project Workflow**
1. **Data Collection**: 
   - Imported ride data from OLA in CSV format.
2. **Data Cleaning and Transformation (SQL)**: 
   - Removed duplicates, handled missing values, and normalized data.
3. **Data Analysis (SQL)**: 
   - Analyzed key metrics such as ride frequency, peak hours, revenue per ride, and customer preferences.
4. **Dashboard Creation (Power BI)**: 
   - Designed a Power BI dashboard to visualize the analyzed data with interactive charts and filters.

### **Dashboard Components**
The Power BI dashboard includes the following visual components:
- **Total Rides**: Displays the total number of rides completed.
- **Revenue Trends**: Shows daily, weekly, and monthly revenue trends.
- **Ride Frequency by Time**: Highlights peak ride hours.
- **Customer Segmentation**: Categorizes customers based on ride frequency and total spending.

### **SQL Queries Used for Analysis**
1. **Retrieve all successful bookings:**
   ```sql
   SELECT * FROM bookings WHERE Booking_Status = 'Success';
   ```
2. **Find the average ride distance for each vehicle type:**
   ```sql
   SELECT Vehicle_Type, AVG(Ride_Distance) AS avg_distance FROM bookings GROUP BY Vehicle_Type;
   ```
3. **Get the total number of cancelled rides by customers:**
   ```sql
   SELECT COUNT(*) FROM bookings WHERE Booking_Status = 'Cancelled by Customer';
   ```
4. **List the top 5 customers who booked the highest number of rides:**
   ```sql
   SELECT Customer_ID, COUNT(Booking_ID) AS total_rides FROM bookings GROUP BY Customer_ID ORDER BY total_rides DESC LIMIT 5;
   ```
5. **Get the number of rides cancelled by drivers due to personal and car-related issues:**
   ```sql
   SELECT COUNT(*) FROM bookings WHERE Cancelled_Rides_by_Driver = 'Personal & Car related issues';
   ```
6. **Find the maximum and minimum driver ratings for Prime Sedan bookings:**
   ```sql
   SELECT MAX(Driver_Ratings) AS max_rating, MIN(Driver_Ratings) AS min_rating FROM bookings WHERE Vehicle_Type = 'Prime Sedan';
   ```
7. **Retrieve all rides where payment was made using UPI:**
   ```sql
   SELECT * FROM bookings WHERE Payment_Method = 'UPI';
   ```
8. **Find the average customer rating per vehicle type:**
   ```sql
   SELECT Vehicle_Type, AVG(Customer_Rating) AS avg_customer_rating FROM bookings GROUP BY Vehicle_Type;
   ```
9. **Calculate the total booking value of rides completed successfully:**
   ```sql
   SELECT SUM(Booking_Value) AS total_successful_value FROM bookings WHERE Booking_Status = 'Success';
   ```
10. **List all incomplete rides along with the reason:**
    ```sql
    SELECT Booking_ID, Incomplete_Rides_Reason FROM bookings WHERE Incomplete_Rides = 'Yes';
    ```

### **Power BI Visual Components**
The Power BI dashboard includes various visuals that address business questions:
1. **Ride Volume Over Time**: A time-series chart showing the number of rides per day/week.
2. **Booking Status Breakdown**: A pie or doughnut chart displaying the proportion of different booking statuses (success, cancelled by the customer, cancelled by the driver, etc.).
3. **Top 5 Vehicle Types by Ride Distance**: A bar chart ranking vehicle types based on the total distance covered.
4. **Average Customer Ratings by Vehicle Type**: A column chart showing the average customer ratings for different vehicle types.
5. **Cancelled Rides Reasons**: A bar chart that highlights the common reasons for ride cancellations by customers and drivers.
6. **Revenue by Payment Method**: A stacked bar chart displaying total revenue based on payment methods (Cash, UPI, Credit Card, etc.).
7. **Top 5 Customers by Total Booking Value**: A leaderboard visual listing customers who have spent the most on bookings.
8. **Ride Distance Distribution Per Day**: A histogram or scatter plot showing the distribution of ride distances for different dates.
9. **Driver Rating Distribution**: A box plot visualizing the spread of driver ratings for different vehicle types.
10. **Customer vs. Driver Ratings**: A scatter plot comparing customer and driver ratings for each completed ride, analyzing correlations.

### **Insights and Findings**
- Most rides occur during peak hours (8 AM - 10 AM and 5 PM - 8 PM).
- Revenue spikes during weekends.
- A significant number of customers take regular rides, indicating a loyal customer base.

### **Challenges Faced**
- Handling missing and inconsistent data during the cleaning process.
- Optimizing SQL queries for large datasets.
- Designing a user-friendly and insightful Power BI dashboard.

### **Future Enhancements**
- Integrate real-time data feeds into the Power BI dashboard.
- Add predictive analytics using machine learning models.
- Enhance customer segmentation using advanced clustering techniques.

### **Key Skills Demonstrated**
- SQL Querying and Data Analysis
- Data Cleaning and Transformation
- Dashboard Design in Power BI
- Data Visualization
- Business Intelligence

### **Project Repository**
You can access the complete project files, including the SQL queries and Power BI dashboard file, in this repository.

**GitHub Repository Link:** [Your Repository Link Here]

### **How to Run the Project**
1. Clone the repository:
   ```bash
   https://github.com/AkshatJain872/OLA-Data-Analytics-Project.git
   ```
2. Import the data into your SQL database.
3. Run the SQL queries provided to process the data.
4. Open the Power BI file to view the interactive dashboard.

---


