# Hotel Bookings and Cancellations Analysis Report

## Table of Contents

- [Project Overview](#project-overview)
- [Steps Taken](#steps-taken)
- [Data Sources](#data-sources)
- [Calculations and Findings](#calculations-and-findings)
- [Recommendations](#recommendations)

### Project Overview

In this project, I've analyzed the number of people booking the hotel annually and the factors influencing bookings and cancellations, as well as the categories of people making these bookings. The objective of this report is to analyze hotel bookings and cancellations to identify patterns, understand guest behavior, and provide recommendations to minimize cancellations and improve overall booking rates.

### Steps Taken

Data Cleaning and Preparation: I've removed columns that were not relevant to the analysis to ensure a focused approach on the key factors affecting bookings and cancellations. Removed columns are- 
lead_time, arrival_date_week_number, arrival_date_day_of_month, stays_in_weekend_nights, stays_in_week_nights, meal, market_segment, distribution_channel, is_repeated_guest, previous_cancellations, previous_bookings_not_canceled, booking_changes, deposit_type, agent, company,
days_in_waiting_list, customer_type, adr, required_car_parking_spaces, total_of_special_requests, adr, customer_type, days_in_waiting_list,
company, agent, deposit_type, booking_changes, previous_bookings_not_canceled, is_repeated_guest.


Null Value Check: 

I checked for null values in the dataset and found none, ensuring the data was complete and ready for analysis.

Data Transformation:

I examined whether guests received their desired room type or not and categorized the guests into types such as family, couples, or singles.
To achieve this, I created a new column named room_status to indicate whether the reserved room type matched the assigned room type. The formula used was:

room_status = IF([@reserved_room_type] = [@assigned_room_type],"Desired","Un-Desired")

Additionally, I created another column named Guest_Type to categorize guests based on their booking patterns using the formula:

Guest_Type = IF(AND(E2 = 2, F2 = 0, G2 = 0), "Couples", IF(AND(E2 = 1, F2 = 0, G2 = 0), "Single", "Family"))

This setup allowed us to perform a deeper analysis of cancellations based on room type preference and guest demographics.

### Data Sources

Hotel Booking/Cancellations Data: The primary dataset used for this analysis is the "hotel_bookings.csv" file, containing detailed information about each booking and cancellation made by the guest and is attached in this repo.

### Calculations and Findings

![Visualization](https://github.com/user-attachments/assets/f6892761-201d-44c3-ac26-9c10e2a0a997)


1. Total Bookings Vs Total Cancellations-

Total Bookings: 119,390
Total Cancellations: 44,224

The percentage of cancellations is approximately 37.04%. This indicates that more than one-third of the total bookings are canceled, highlighting a significant area for improvement.

2. Cancellations with Respect to Guest Type-

The cancellation percentages for each guest type are as follows:

Couples: 39.75%

Family: 34.39%

Singles: 29.03%

Couples have the highest cancellation rate at 39.75%, followed by families and singles. This suggests that couples are more likely to cancel their bookings compared to other guest types. Understanding the reasons behind this behavior can help in formulating strategies to reduce cancellations.

3. Impact of Room Allocation on Cancellations-

The desired room type has a higher cancellation rate of approximately 41.56%.

This finding suggests that the mismatch between the room reserved by the guest and the room actually allocated does not significantly impact the overall cancellation rate. Guests appear to be less concerned about receiving a different room type than they initially desired.

4. Cancellations by State-

The bar chart analysis shows that each state has a similar cancellation rate, indicating a uniform pattern of cancellations across different locations.

States with the highest booking rates include Maharashtra, Uttar Pradesh, and Bengal. These states also tend to have a higher number of cancellations, potentially due to their higher volume of bookings.

5. Cancellations Based on Months-

The graph analysis reveals that people prefer traveling during the summer season, with the highest booking rates in May, June, July, and August.
During these months, the cancellation rate is relatively low compared to the number of bookings, indicating a stronger commitment to travel plans during the summer season.

### Recommendations
To reduce cancellations and increase hotel bookings, the following strategies are recommended:

Enhance Customer Experience: Focus on personalized offers, improved communication, and flexible check-in/check-out options to improve guest satisfaction and reduce cancellations.

Offer Incentives for Non-Cancellation: Provide discounts for non-refundable bookings and introduce loyalty programs that reward guests who do not cancel their reservations.

Improve Booking and Cancellation Policies: Develop more flexible booking options, such as partial refunds or tiered cancellation fees, to encourage guests to retain their bookings.

Enhance Online Presence and Booking Process: Optimize the hotel’s website and mobile app for a seamless booking experience, and offer multiple payment options to reduce booking abandonment.

Promote Direct Bookings: Encourage direct bookings through the hotel’s website by offering exclusive perks and a best-rate guarantee.

Targeted Marketing Campaigns: Use data-driven marketing strategies to reach specific customer segments and reduce cancellations, especially during high booking periods.
