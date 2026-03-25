# G-plast Sales Dashboard

A comprehensive, interactive sales analytics dashboard for G-plast, providing real-time insights into sales performance across multiple units, territories, and customers.

## 📊 Features

### 1. **Monthly Overview**
- Combined monthly sales chart for all units
- Stacked bar chart showing sales breakdown by department (IMD, DCD, TRD, MED)
- Department share doughnut chart
- Export monthly data to Excel

### 2. **Day-wise Sales**
- Daily sales bar chart with all dates displayed (no gaps)
- Filter by:
  - Month (all months or specific month)
  - Unit (IMD, DCD, TRD, MED)
  - Territory (Export, Domestic, General)
- Shows sales statistics (days with sales, total amount)
- Export daily data to Excel

### 3. **Customer Analysis**
- **Top Customers Horizontal Bar Chart** (Top 10 or Top 20 based on selection)
- **Bottom 10 Customers Horizontal Bar Chart** (lowest performing customers)
- **Customer Sales Overview Vertical Bar Chart** (Top 10 or Top 20)
- **Customer Day-wise Sales** (specific customer sales over time)
- Export options for:
  - Top customers (10,20 ranking selection)
  - Bottom 10 customers
  - Selected customer's daily sales

### 4. **KPI Cards**
Quick overview of key metrics:
- Grand Total Sales
- Department-wise totals (IMD, DCD, TRD, MED)
- Territory-wise totals (Export, Domestic, General)
- Percentage contribution of each department

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Excel file named `data.xlsx` in the same directory as the HTML file

### Installation

1. **Download the Dashboard**
   - Save the HTML file as `index.html`

2. **Prepare Your Data**
   - Ensure your Excel file is named `data.xlsx`
   - Place it in the same folder as the HTML file

3. **Excel File Format**
   Required columns in your Excel file:
   - `Inv. Date` - Invoice date (DD.MM.YYYY or date format)
   - `Unit` - Department/Unit name (IMD, DCD, TRD, MED) // hardcoded
   - `Territory` - Territory (EXPORT, DOMESTIC, GENERAL)
   - `Sale Amt.` or `Sale Amt` - Sales amount
   - `Benf. Name` or `Benf Name`

4. **Open the Dashboard**
   - Double-click the HTML file or open it in your browser
   - The dashboard will automatically load and parse `data.xlsx`

## 📁 File Structure
```
project-folder/
├── index.html          # Main dashboard file
└── data.xlsx              # Your sales data file
```

## 🎨 Dashboard Sections

### Header Section
- Dashboard title with click-to-reset functionality
- Data statistics (valid rows count)
- Last updated timestamp
- Manual refresh button

### Tabs Navigation
- **Monthly Overview** - Monthly aggregated data
- **Day-wise** - Daily sales with filters
- **Customer Analysis** - Detailed customer insights


## 🔧 Technologies Used

- **HTML5** - Structure
- **CSS3** - Styling with CSS variables and responsive design
- **JavaScript** - Core functionality
- **Chart.js 4.4.1** - Data visualization
- **SheetJS (XLSX) 0.18.5** - Excel file parsing
- **Google Fonts (Inter)** - Typography

## 📱 Responsive Design

The dashboard is fully responsive and optimized for:
- Desktop (1400px+)
- Laptop (900px - 1400px)
- Tablet (600px - 900px)
- Mobile (< 600px)
- Small mobile (< 380px)

## 🎯 Key Features in Detail

### All Dates Display
- When a specific month is selected, shows ALL days of that month (1-31, 1-30, or 1-28/29)
- Zero sales days appear as empty bars
- No gaps or skipped dates

### Horizontal Bar Charts
- Customer names on Y-axis (easier to read)
- Sales amounts on X-axis
- Truncated names with full name on hover
- Ideal for displaying multiple customers

### Toast Notifications
- Animated notifications with close button
- Color-coded messages:
  - 🟢 Success (green)
  - 🟡 Warning (yellow)
  - 🔴 Error (red)
  - 🟣 Info (purple)
- Auto-dismiss after 4 seconds

## 📊 Data Processing

The dashboard automatically:
1. Reads Excel file using SheetJS
2. Parses dates to standard format
3. Normalizes territory names (EXPORT, DOMESTIC, GENERAL)
4. Aggregates sales by date, customer, unit, territory
5. Handles missing or invalid data gracefully

## ⚡ Performance Tips

- Charts are destroyed and recreated on update (prevents memory leaks)
- Data filtering is optimized using Map objects
- Responsive design ensures smooth rendering on all devices
- Lazy loading of charts when switching tabs

## 🐛 Troubleshooting

### Common Issues

1. **"Could not load data file" error**
   - Ensure `data.xlsx` is in the same folder as the HTML file
   - Check file name is exactly `data.xlsx` (case-sensitive)
   - Verify file is not corrupted

2. **No data showing**
   - Check Excel column names match required format
   - Ensure dates are properly formatted
   - Verify sales amounts are numeric

3. **Charts not rendering**
   - Clear browser cache and reload
   - Check browser console for errors
   - Ensure internet connection for Chart.js CDN

4. **Dates showing incorrectly**
   - Excel dates should be in DD.MM.YYYY format or Excel date numbers
   - The dashboard handles multiple date formats

## 🔒 Browser Compatibility

| Browser |   Support |
|---------|---------|---------|
| Chrome  |     ✅ Full |
| Firefox |     ✅ Full |
| Safari  |     ✅ Full |
| Edge    |     ✅ Full |
| Opera   |     ✅ Full |
| comet   |     ✅ Full |

## 📊 Sample Data Structure

Your Excel file should look like this:

| Inv. Date | Unit | Territory | Sale Amt. | Benf. Name |
|-----------|------|-----------|-----------|------------|
| 01.01.2024 | IMD | DOMESTIC | 25000 | ABC Company |
| 02.01.2024 | DCD | EXPORT | 45000 | XYZ Corp |
| 03.01.2024 | TRD | GENERAL | 15000 | DEF Ltd |

---
**Last Updated:** March 2026
```


