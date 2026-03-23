# G-plast Sales Dashboard

## 📁 File Names

- **Dashboard file:** `dashboard.html` (or any name you prefer)
- **Data file:** `data.xlsx` (MUST be exactly this name)

## 📁 Tech stack

        - HTML
        - CSS
        - JavaScript
        - SheetJS (for Excel file reading)
        - Chart.js (for data visualization)
        - React.js (for dashboard components)
        - FMR Currency (for currency conversion)

        
## 📁 Folder Structure

your-project-folder/
│
├── dashboard.html # The main dashboard file
├── data.xlsx # Your sales data (EXACT name)
└── README.md # This file

## 📊 Supported Column Names

The Excel file MUST have these columns (spelling matters):

### ✅ Required Columns:

| Data Needed   | Accepts These Column Names                            |
| ------------- | ----------------------------------------------------- |
| **Date**      | `Inv. Date` , `Inv Date` , `Invoice Date`             |
| **Unit**      | `Unit` , `Dept` , `Department`                        |
| **Territory** | `Territory` , `Teritory`                              |
| **Amount**    | `Total Amt` , `TotalAmt` (last column with this name) |

### ✅ Your Excel Should Have:

- `Inv. Date` ✓
- `Unit` ✓
- `Territory` ✓
- `Total Amt` (at the end) ✓

## 🚀 How to Use

### 1️⃣ Setup Files

1. Place `dashboard.html` and `data.xlsx` in the **same folder**
2. Make sure your Excel file is named exactly `data.xlsx`

### 2️⃣ Open Dashboard

**Option A: Using Live Server (Recommended)**

- Install "Live Server" extension in VS Code
- Right-click on `dashboard.html` → "Open with Live Server"

```

### 3️⃣ View Dashboard
- Dashboard will load automatically
- Click **"Refresh Data"** button to reload data
- Switch between **Monthly** and **Day-wise** tabs

## 📥 Export Features

### Excel Export
- **Monthly Tab:** Click "Export Monthly to Excel"
  - Exports: Month, IMD, DCD, TRD, MED, Total
- **Daily Tab:** Click "Export Daily to Excel"
  - Exports: Date, Amount, Unit, Territory (with current filters applied)

## 📊 Dashboard Features

### KPI Cards
- Grand Total (all sales)
- IMD, DCD, TRD, MED breakdown
- Export, Domestic, General sales

### Monthly Overview Tab
- Combined monthly sales chart
- Stacked chart by units
- Department share (pie chart)

### Day-wise Tab
- Filter by: Month, Unit, Territory
- Shows full dates (e.g., "01 Jan 2024")
- Days with ₹0 sales shown in gray

## ⚠️ Important Notes

### File Requirements
- **File name:** MUST be `data.xlsx` (case-sensitive)
- **File location:** Same folder as dashboard.html
- **DO NOT:** Double-click HTML file (use Live Server instead)

### Data Format
- Dates should be in Excel date format
- Amounts should be numbers (not text)
- Valid units: IMD, DCD, TRD, MED
- Valid territories: EXPORT, DOMESTIC, GENERAL

### Column Matching
- Column names are **case-insensitive** (`Inv. Date` = `inv date`)
- If you have multiple "Total Amt" columns, the **last one** is used
- Extra columns are ignored (won't cause errors)

## 🔧 Troubleshooting

### "Could not load data file" Error
✅ Check if `data.xlsx` is in the same folder as `dashboard.html`
✅ Make sure file name is exactly `data.xlsx`
✅ Open via Live Server (not by double-clicking)
✅ Check browser console (F12) for detailed errors

### "No valid rows found" Error
✅ Check column names match the supported names above
✅ Ensure dates are in Excel date format (not text)
✅ Verify amounts are numbers
✅ Check that Unit and Territory columns have valid values

### Charts Not Displaying
✅ Click "Refresh Data" button
✅ Try different browser (Chrome recommended)
✅ Clear browser cache (Ctrl+Shift+R)

### Export Not Working
✅ Make sure you're viewing a chart first
✅ Check if browser is blocking downloads
✅ Try clicking export button again
## 🎨 Features

### Data Filters (Day-wise Tab)
- Month dropdown (All Months or specific month)
- Unit filter (All Units or IMD/DCD/TRD/MED)
- Territory filter (All or Export/Domestic/General)
- Real-time chart updates

## 📝 Data Privacy
- All data processing happens in your browser
- No data is sent to any server
- Data file stays on your computer
- Safe to use with sensitive business data

## 🔄 Updating Data
1. Edit your `data.xlsx` file
2. Save the file
3. Click **"Refresh Data"** button in dashboard
4. Dashboard updates automatically

## 💡 Tips for Best Results
- Keep Excel file under 5MB for fast loading
- Use consistent date formats
- Avoid blank rows in Excel
- Close Excel file before refreshing dashboard
- Use latest Chrome/Firefox for best performance

---
**Supported Browsers:** Chrome, Firefox, Edge, Safari (latest versions)
```
