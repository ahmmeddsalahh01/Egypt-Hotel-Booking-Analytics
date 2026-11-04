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

## Advanced Recommendations

1. **Test ways to lift February demand.** February is the lowest-revenue month shown (257K), while October is highest (310K). Test targeted February packages, such as weekday stays or local-experience bundles. Compare bookings, occupancy, average daily rate, and net revenue with similar dates before expanding the offer.

2. **Reduce cancellations and no-shows.** The dashboard shows a 14.8% cancellation rate and a 7.7% no-show rate. Send timely booking confirmations and pre-arrival reminders, make it easy for guests to confirm or change plans, and offer released rooms to a waitlist. Pilot deposits or booking guarantees on selected booking types, then measure completed stays, recovered room revenue, and guest complaints.

3. **Increase suitable room upgrades.** Executive Suites generate the largest displayed room-type revenue share (32.29%). Train booking and front-desk staff to offer relevant upgrades when availability allows. Track upgrade acceptance, occupancy, average daily rate, and the added service costs to confirm the offers improve profit.

4. **Manage channels by net revenue.** Online Travel Agencies show the highest displayed channel revenue (691K), followed by Direct (646K), Walk-in (638K), and Phone (612K). Compare each channel’s revenue after commission, acquisition costs, cancellations, and no-shows. Encourage repeat guests to book direct with useful benefits, while retaining third-party channels that bring profitable demand.

5. **Build repeat visits and improve guest profiles.** The loyalty chart assigns 41.3% of revenue to a blank tier, while Silver accounts for 32.02%. Invite guests to complete their profiles and explain the benefits of joining the loyalty program. Test relevant return-visit offers and track profile completion, repeat bookings, and net revenue per guest.

6. **Use hotel performance comparisons to guide reviews.** Nile View Grand and Marina Bay lead the displayed hotel revenue figures, while Desert Rose Inn has the highest displayed revenue per available room. Compare pricing, occupancy, room mix, capacity, and operating costs across properties before transferring practices or setting hotel targets.

7. **Align staffing with arrival patterns.** Wednesday has the most check-ins in the weekday chart (1,042), and October has the most monthly check-ins shown (644). Use arrival forecasts to plan front-desk and housekeeping coverage, then monitor room readiness, guest wait times, and labor costs to see whether schedules are improving service efficiently.

8. **Validate market-specific promotions before scaling.** The dashboard shows differences in average guest spend by country and guest preferences across hotel cities. Test a small number of relevant offers with clearly defined guest groups. Check group sizes and booking value as well as average spend so that small samples do not drive broad marketing decisions.

9. **Reconcile the dashboard measures before setting business targets.** The booking count and revenue totals differ between the workbook and dashboard visuals. Confirm the filters, booking statuses, and measure definitions behind each KPI, then use a consistent definition for revenue, cancellations, no-shows, and lost revenue in future reporting.

## Tools

 Microsoft Power BI Desktop (`.pbix` report)
 Microsoft Excel (`.xlsx` source workbook)
