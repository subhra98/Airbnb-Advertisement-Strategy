# Airbnb Advertisement Strategy: Power BI Dashboard

A four-page Power BI dashboard that analyses Airbnb user behaviour, the booking funnel and revenue, and turns the findings into data-backed recommendations for ad spend.

**Data period:** 5 May 2014 to 23 April 2015

---

## Headline KPIs

| Total visits | Unique visitors | Total bookings | Total revenue | Conversion rate |
|:---:|:---:|:---:|:---:|:---:|
| 7,756 | 630 | 984 | $245.11K | 31.58% |

Average booking value: **$249.10**. Each visitor visits about 12 times and books about 1.6 times.

---

## Business problem

Where should Airbnb focus its advertising budget? Who are the users, when and on what device do they arrive, where does the booking funnel leak, and which users generate the revenue?

---

## Dashboard pages

| Page | Purpose | Main visuals |
|---|---|---|
| **1. EDA** | Headline KPIs and traffic picture | KPI cards, date slicer, treemap (users by app), users by device, gender pie, conversion gauge, sessions trend |
| **2. User Demographics** | Who the users are and what they spend | Age histogram, age vs revenue scatter, top 10 streets by searches, day-of-week by device heatmap, average spent |
| **3. Temporal & Booking Trends** | When users engage and what drives conversion | Decomposition tree, monthly clicks/bookings/conversion line chart, sessions by day of week |
| **4. Performance & Revenue Insights** | Where the funnel leaks and who pays | Conversion funnel, device performance combo chart, potential customers lost by device, revenue share donut |

All pages have date, device and gender filters that cut across the visuals.

<!-- Add screenshots to an /assets folder and update the paths below -->
![EDA](assets/page1_eda.png)
![User Demographics](assets/page2_demographics.png)
![Temporal & Booking Trends](assets/page3_trends.png)
![Performance & Revenue Insights](assets/page4_performance.png)

---

## Data model

Five tables:

- **Dates**: calendar, day types, day names
- **Locations**: location id, street, city, state, latitude, longitude
- **Search Data**: visitor, session, device/app, timestamps, search, message sent, booking request sent, booking amount, left review, next-session fields
- **Unique Users**: visitor id, name, gender, age
- **Stats**: supporting table

---

## Key insights

**Audience**
- Core age group is 25 to 35, peaking near 30. Ages 22 to 35 spend the most, and spending drops significantly after 40.
- Women are 56.1% of users, but the largest single-age booking totals come from male users.

**Traffic**
- iPhone (about 3.4K users) and the iOS app (2.21K users) lead traffic. Desktop is second (about 2.0K).
- Search demand is concentrated on a few San Francisco streets: Mission, Lombard and Market lead.

**Timing**
- Monday is the busiest day. Saturday and Sunday run about 25% below Monday.
- Daily sessions peaked around September 2014 and December 2014 to January 2015.

**Conversion**
- Funnel: 3,116 searches → 1,279 messages (41%) → 984 booking requests (77%).
- The biggest leak is search to message: about 59% of searches never reach a message.
- Conversion by device: Desktop 47%, iPad 46%, Android phone 40%, **iPhone 21%**, Other 16%, Android tablet 13%.
- Within Desktop, Web (13%) and Moweb (12%) are weak spots against 40% to 70% for other browsers.
- About 885 iPhone searches did not become bookings, the largest retargeting pool.

**Revenue**
- Returning users generate **84.95%** of revenue and new users 15.05%.

---

## Recommendations

| # | Action | Priority |
|---|---|---|
| 1 | Age-targeted, geo-targeted video ads (premium stays for 30 to 35, budget stays for 22 to 30) | High |
| 2 | Fix the iPhone booking flow, then scale spend | High |
| 3 | Concentrate campaigns on Monday and Wednesday, cut weekend spend | Medium |
| 4 | Add safety and trust features to lift search-to-message conversion | High |
| 5 | Retargeting and retention programme for lost-before-booking users and past guests | High |
| 6 | Improve Web and Moweb experience | Medium |

**Illustrative opportunity:** if iPhone conversion rose from 21% to the Desktop level of 47%, it could add roughly 294 bookings (about $73K), around 30% uplift on total revenue. This is a scenario, not a forecast.

---

## Limitations

- Some values (users by device, searches and bookings by device, weekday sessions, top streets) were read from charts without data labels and are approximate.
- Only one year of data, so seasonality cannot be confirmed.
- No ad cost or channel data, so ROAS and cost per booking cannot be calculated.
- The dashboard note saying male users dominate conflicts with the 56.1% female share on the gender pie.
- The overall conversion (31.58%, bookings / searches) and the monthly chart (reaches 100%) appear to use different denominators.

---

## Tools and skills

Power BI Desktop, DAX, data modelling, data visualisation, exploratory data analysis, funnel analysis, customer segmentation, business storytelling.

---

## Repository structure

```
├── Airbnb.pbix          # Power BI dashboard
├── Airbnb.pdf           # Detailed analysis report
├── Airbnb.pptx          # Presentation
├── assets/              # Dashboard screenshots
└── README.md
```

## How to use

1. Download `Airbnb.pbix`.
2. Open it in Power BI Desktop (Windows).
3. Use the date, device and gender slicers to explore each page.

---

## Next steps

- Add ad cost, campaign and channel fields to measure return on ad spend.
- Add returning vs new user counts to calculate lifetime value.
- Align the conversion definition across pages and correct the gender annotation.
- Extend the dataset beyond one year.

---

## Author

**Subhrajyoti Bera** · [LinkedIn]([https://linkedin.com/in/your-profile](https://www.linkedin.com/in/subhrajyotibera/)
