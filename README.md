# Egypt Hotel Booking Analytics

## Small overview

An interactive Power BI project exploring booking patterns, hotel revenue, cancellations, payment and booking channels, and guest behavior across a generated practice dataset representing hotels in Egypt. The dataset is for learning and demonstration; it does not describe real hotels or guests.

## Business questions

 How do bookings and revenue change over time?
 Which hotels, cities, and room types contribute the most revenue?
 What are the cancellation and no-show rates, and how do they vary by month, booking lead time, and channel?
 Which booking channels and payment methods are associated with higher revenue or booking value?
 How do guest country and loyalty tier relate to spending and hotel preferences?
 When do guests check in, and how long do they stay?

## Data

The project includes `hotel_booking_raw.xlsx`, organized into four sheets:

 `fact_bookings`  9,050 booking records, including booking and check-in dates, stay length, guest count, total amount, status, payment method, and booking channel
 `dim_hotel` 8 hotel records with city, star rating, and room capacity
 `dim_room_type`  44 room type records with hotel, room name, base price, and maximum occupancy
 `dim_guest`  400 guest records with country, loyalty tier, and signup date

The data is generated practice data. Figures below are the values displayed in the supplied dashboard and should be interpreted as illustrative.

## Data cleaning

The supplied workbook is arranged as a booking fact table and three descriptive tables for hotels, room types, and guests. This structure supports analysis by booking, hotel, room type, and guest attributes.

The project files do not document specific cleaning steps such as duplicate removal, missing-value handling, or outlier treatment. Those steps should be confirmed and documented before treating the data model as fully validated. The dashboard also displays a blank payment-method category, which should be checked and either explained or handled explicitly.

## Dashboard pages

1. **Landing Page**  report navigation.
2. **Home Page**  headline booking and revenue KPIs, average booking value, and monthly revenue trend.
3. **Revenue and performance**  revenue by hotel, room type, and city, plus revenue per available room.
4. **Cancellations and no-shows**  cancellation and no-show KPIs, monthly cancellation trend, cancellation by lead time, and by channel.
5. **Channels and payments**  booking value and revenue comparisons by payment method and booking channel.
6. **Guests**  top guests by revenue, revenue by loyalty tier, country and hotel-city preferences, and average spend by country.
7. **Booking behavior**  stay length, lead time, check-in month, and check-in weekday patterns.

## Detailed key findings

- The Home Page displays **9,000 total bookings**, **2.67M revenue**, **515.91K lost revenue**, and an **average booking value of 384**.
- Monthly revenue on the Home Page ranges from **257K in February** to **310K in October**. March is also high at **306K**.
- The Cancellations and no-shows page displays a **14.8% cancellation rate** and a **7.7% no-show rate**. The monthly cancellation chart peaks at **16.0%** in February and September and reaches its low of **12.4%** in December.
- Booking behavior KPIs show an **average stay of 3 nights**, a **median lead time of 30 days**, and an **average lead time of 29.86 days**. Wednesday has the most check-ins in the weekday chart (**1,042**).
- The Guests page displays **400 unique guests**. Emily Müller is the top guest by realized revenue in the chart at about **12K**. Silver-tier guests account for the largest shown share of revenue (**32.02%**).
- On the Revenue and performance page, the room-type chart shows **3.46M total revenue**. Executive Suites are the largest room-type segment at **1.12M (32.29%)**. Nile View Grand has the highest hotel revenue in the chart at about **357K**, narrowly ahead of Marina Bay Resort at **356K**.
- The revenue-per-available-room chart ranks Desert Rose Inn highest at approximately **3,348**.
- **The headline metrics do not currently reconcile:** the workbook has 9,050 booking rows while the Home Page shows 9,000 bookings, and the Home Page shows 2.67M revenue while the room-type chart totals 3.46M. These figures may use different filters or measure definitions; verify them before drawing conclusions.

## Advanced recommendations

 **Define and reconcile measures:** document whether revenue means booked, realized, or net revenue; specify treatment of cancelled and no-show bookings; reconcile booking counts against the source rows; and show the same definition wherever a KPI is reused.
 **Build a cancellation risk view:** compare cancellation rates across lead-time bands, channels, month, hotel, and room type. If a prediction model is added later, evaluate it on a held-out time period and use its scores to guide review or reminder policies rather than treating predictions as certainty.
 **Add operational context to revenue:** pair revenue per available room with occupancy, available rooms, and average daily rate. Use these together to distinguish high revenue from high utilization or higher pricing.
 **Measure channel value after costs:** compare realized revenue, average booking value, cancellation rate, and acquisition or commission cost by channel. The current report does not show channel costs, so revenue alone cannot identify the most profitable channel.
 **Improve guest segmentation:** compare repeat-booking rate and spend by country and loyalty tier, then test targeted offers on small groups. The supplied practice data supports demonstration only, not real customer targeting.
 **Add data-quality checks:** validate keys and relationships between the four tables, check missing categories and dates, and add a refresh-time summary of row counts and rejected records.
 **Clarify chart labels and units:** fix the payment chart whose axis says “Booking Channel” although the visual is titled “Average Booking Value by Payment Method”; show currency and time-period units consistently.

## Tools

 Microsoft Power BI Desktop (`.pbix` report)
 Microsoft Excel (`.xlsx` source workbook)
