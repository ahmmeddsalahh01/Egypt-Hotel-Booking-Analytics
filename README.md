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

1. **Plan campaigns around the displayed seasonal pattern.** February is the lowest-revenue month in the Home Page, while October is the highest. Test a targeted February offer—such as a weekday stay package or local attraction bundle—and prepare staffing and room availability ahead of October. Compare incremental net revenue, occupancy, and average daily rate with comparable dates; do not assume a single year's pattern will repeat.
2. **Reduce cancellations and no-shows.** The report shows a 14.8% cancellation rate and a 7.7% no-show rate. Send a clear confirmation and pre-arrival reminder, make it easy for guests to confirm or change plans, and offer a waitlist for released rooms. Pilot any deposit or guarantee policy on selected booking types, then compare cancellation and no-show rates alongside completed stays, guest complaints, and net revenue.
3. **Grow higher-value room bookings through service-led upselling.** Executive Suites contribute the largest displayed share of room-type revenue (32.29%). Train reservation staff to offer suitable upgrades and packages when availability allows. Track upgrade conversion, occupancy, average daily rate, and contribution after service and discount costs so higher room revenue also benefits the hotel.
4. **Compare booking channels by net contribution.** Online Travel Agency bookings show the highest displayed channel revenue, while Direct, Phone, and Walk-in channels also contribute materially. Maintain channels that bring profitable demand; encourage repeat guests to book direct with useful benefits such as flexible check-in or a loyalty perk. Compare net revenue after commissions, cancellation rates, and guest acquisition costs before shifting channel spend.
5. **Improve guest recognition and repeat stays.** The Guests page shows a substantial revenue share in the blank loyalty-tier category. Invite guests to provide their loyalty status during booking or check-in, then use relevant post-stay offers and return-visit benefits. Track profile completion, repeat-booking rate, and net revenue per guest while respecting guest consent.
6. **Use guest markets to shape offers.** The dashboard compares guest country, hotel-city preferences, and average spend by country. Create a small number of market-specific packages—for example, city-and-resort combinations where the preference data supports them—and test them with a limited campaign. Check booking counts and spend per guest together so small groups do not drive misleading conclusions.
7. **Use hotel performance to guide local operating reviews.** Nile View Grand has the highest displayed hotel revenue, and Desert Rose Inn ranks highest in revenue per available room. Compare their pricing, room mix, occupancy, and service practices with other properties. Share practices that improve contribution, but account for room capacity and operating costs before setting cross-hotel targets.
8. **Schedule staffing for check-in demand.** Wednesday has the most check-ins in the weekday chart. Align front-desk coverage and housekeeping handoffs with expected arrivals, then track wait times, room readiness, and labor cost by arrival day to see whether the schedule improves service efficiently.

## Tools

 Microsoft Power BI Desktop (`.pbix` report)
 Microsoft Excel (`.xlsx` source workbook)
