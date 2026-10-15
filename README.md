# 📊 AdventureWorks – Sales Performance Report

An end-to-end, executive-ready Power BI sales analytics report transforming raw database structures into a polished, SaaS-style management dashboard for strategic decision-making.

---

## 📸 Dashboard Overview


<img width="1920" height="1079" alt="page1" src="https://github.com/user-attachments/assets/fb56f508-2068-4569-968f-d51e961aea43" />
<img width="1915" height="1080" alt="page2" src="https://github.com/user-attachments/assets/3b1520c2-11a0-4cad-b934-22eab87b80fa" />
<img width="1917" height="1080" alt="page3" src="https://github.com/user-attachments/assets/2c78f7ce-c44d-4a98-b197-168b26282324" />
<img width="1917" height="1078" alt="page4" src="https://github.com/user-attachments/assets/f065d81c-82d9-40a5-b2e1-71c1b702ab54" />

### 🔍 Interactive Drill-Down Capabilities

The report leverages multi-level visuals enabling executives to seamlessly drill down from high-level summaries into granular dimensions:

<img width="1914" height="1080" alt="page2_1" src="https://github.com/user-attachments/assets/9e0ad630-aec1-4caa-a3d0-61154e20a932" />
<img width="1921" height="1079" alt="page3_1" src="https://github.com/user-attachments/assets/f33b0ba3-af9e-4c41-adef-7f5e27892806" />

- **Geographic Exploration:** Country-level drill-down revealing regional sales distribution (e.g., US Sales broken down by Southwest, Northwest, etc.).
- **Product Hierarchy:** Dynamic drill-down from Product Category down to Subcategory and Model levels.
- **Dynamic Color Inheritance:** Visual indicators automatically recalculate colors and metrics based on the active aggregation level using custom DAX logic.

> **Note on Live Interactive Demo:** Public "Publish to Web" embedding is restricted by organizational tenant security policies. You can download and inspect the fully functional `.pbix` file (`AdventureWorks_Sales_Performance_Report.pbix`) directly from this repository to explore the dynamic model, DAX measures, and UI interactions in Power BI Desktop.

---

## 🌟 Key Business Features & Analytics

- **Executive Summary:** High-level executive grid featuring core business metrics: `Total Sales`, `Total Profit`, `Total Quantity`, and `Profit Margin %`.
- **Profitability Metrics:** Dynamic `Profit Margin %` calculation built with safe DAX patterns (`DIVIDE`) to assess true operational performance.
- **Closed-Period vs. All-Time Logic:** Strategic differentiation between full historical dataset views and dynamic closed-period reporting logic.
- **Product Hierarchy & Drill-Down:** Interactive Treemap visual enabling seamless navigation from Category down to Subcategory and Model levels.
- **Geographic & Time-Series Views:** Geospatial performance mapping alongside month-over-month trend visualization.

---

## 🎨 Design System & UX Standards

- **Typography & Layout:** Clean grid structure built with Segoe UI (11pt base), consistent alignment, and symmetric KPI positioning across all report pages.
- **SaaS Aesthetic:** Corporate blue palette with muted secondary tones, avoiding high-contrast or harsh visual distraction.
- **Data Hygiene:** Elimination of technical database prefixes (e.g., standardized fields like `Model`, `Month`, `Region`).
- **Interactive Tooltips & States:** Standardized hover, press, and focus states for buttons and icons with consistent decimal and currency formatting.

---

## 🛠️ Tech Stack & DAX Highlights

- **Tooling:** Power BI Desktop, Power BI Service
- **Data Architecture:** Star Schema modeling built on AdventureWorks
- **Key DAX Calculations:**
  - **Profit Margin %**: 
    ```dax
    Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
    ```
  - **Dynamic Visual Formatting:** Custom `SWITCH` statements for conditional color formatting and dynamic axis/kpi highlighting.
- **Supporting Measures:** Includes YoY calculations, dynamic switching, and formatting logic.

---

## 📁 Repository Contents

- `AdventureWorks_Sales_Performance_Report.pbix` — Complete Power BI report source file.
- `AdventureWorks_Sales_Performance_Report.pdf` — Exported multi-page PDF document for quick offline viewing.
- `README.md` — Project documentation and visual presentation.
