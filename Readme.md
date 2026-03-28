# G-plast Sales Dashboard

## Overview
A comprehensive, interactive sales analytics dashboard for G-plast that transforms Excel sales data into actionable insights through beautiful visualizations, real-time filtering, and drill-down capabilities.

## Features

### 📊 Key Performance Indicators (KPIs)
- **Grand Total Sales** with department-wise breakdown (IMD, DCD, TRD, MED)
- **Export vs Domestic** sales comparison
- **Department-level export/import** analytics
- **Animated count-up** effects on load
- **Click-to-filter** drill-down functionality

### 📈 Data Visualizations
- **Monthly Sales Trends**: Combined view and stacked department view
- **Department Share**: Interactive doughnut chart
- **Day-wise Sales**: Daily breakdown with month/unit/territory filters
- **Customer Analysis**: 
  - Top/Bottom 10-20 customers (horizontal bar charts)
  - Customer daily sales timeline
  - Searchable customer dropdown

### 🔍 Interactive Features
- **Multi-level filtering**: Month, Unit (Department), Territory
- **Cross-chart drill-down**: Click any KPI to filter entire dashboard
- **Focus Mode**: Click any chart to enlarge with detailed data table
- **Copy to Clipboard**: Export table data from focus mode
- **Real-time updates**: All charts update instantly on filter changes

### 📤 Export Capabilities
- **Monthly sales** data export (Excel)
- **Daily sales** export
- **Customer overview** export
- **Top/Bottom customers** export
- **Selected customer daily sales** export
- **Button animations** with success feedback

### 🎨 User Experience
- **Glass morphism design** with modern aesthetics
- **Responsive layout** (mobile, tablet, desktop)
- **Loading animations** and state indicators
- **Toast notifications** for all actions
- **Smooth transitions** between tabs and views

## Technology Stack

| Technology | Purpose |
|------------|---------|
| HTML5/CSS3 | Structure & styling with modern CSS features |
| JavaScript (ES6+) | Core application logic |
| Chart.js 4.4.1 | Data visualization library |
| SheetJS (XLSX) 0.18.5 | Excel parsing and export |
| Google Fonts (Inter) | Typography |

## Installation & Setup

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Excel file named `data.xlsx` in the same directory

### Quick Start
1. Clone or download the HTML file to your local machine
2. Place your Excel file (`data.xlsx`) in the same folder
3. Open the HTML file in a web browser
4. The dashboard will automatically load and parse your data

### Excel File Format Requirements
The Excel file should contain the following columns:
- **Inv. Date**: Invoice date (supports DD.MM.YYYY or Excel date format)
- **Unit**: Department (IMD, DCD, TRD, MED)
- **Territory**: Export or Domestic
- **Benf. Name/Benf Name/Customer**: Customer name
- **Sale Amt.** or **Total Amt.**: Sales amount in INR

## Usage Guide

### Navigating the Dashboard
1. **KPI Row**: Click any card to filter by that department or territory
2. **Tabs**: Switch between Monthly, Daily, and Customer views
3. **Filters**: Use dropdowns to refine data by month, unit, or territory
4. **Charts**: Click any chart to open focus mode with detailed data table

### Drill-Down Example
1. Click "IMD" KPI → Dashboard filters to show only IMD sales
2. Click "Export" KPI → Further filters to show IMD Export sales
3. Click "Reset Filters" to return to full view

### Exporting Data
- Click any export button to download filtered data as Excel
- Watch for success animations and toast notifications
- Filenames include context and timestamp

### Customer Analysis
1. Select ranking (Top 10/20 customers)
2. Apply month/unit/territory filters
3. Search for specific customers using the search box
4. Select a customer to view their daily sales timeline

## Technical Implementation Highlights

### Data Processing
- **Smart date parsing**: Handles Excel numeric dates and string formats
- **Field normalization**: Supports multiple column name variations
- **Data validation**: Filters out invalid entries automatically
- **Currency formatting**: Indian numbering system (Lakhs, Crores)

### State Management
- Centralized data store (`allRows` array)
- Chart instance management to prevent memory leaks
- Filter state synchronized across tabs

### Animation System
- **Count-up animations**: RequestAnimationFrame with easing
- **Chart transitions**: 800ms easeOutQuart animations
- **Staggered entries**: CSS custom properties for sequential reveals
- **Button morphing**: Loading states with success indicators

### Focus Mode
- **Chart enlargement**: Full-screen view with detailed table
- **Dynamic table generation**: Context-aware column headers
- **Copy functionality**: Clipboard API with TSV format
- **Scroll locking**: Prevents background scrolling

### Responsive Design
- **Mobile-first approach**: Adapts to all screen sizes
- **Touch-friendly**: Increased tap targets on mobile
- **Fluid typography**: Clamp() for responsive font sizes
- **Canvas scaling**: Maintains aspect ratio across devices

## Performance Optimizations
- Lazy rendering of inactive tabs
- Chart destruction before recreation
- Efficient array filtering (O(n) complexity)
- Debounced resize handlers
- Memory leak prevention

## Error Handling
- **File load errors**: User-friendly error overlay with retry
- **Empty data states**: Informative messages in charts
- **Missing columns**: Graceful fallbacks
- **Clipboard API failures**: Clear error messages

## Browser Support
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+
- Mobile browsers (iOS Safari, Chrome for Android)

## Customization

### Color Themes
Modify CSS variables in `:root`:
```css
--accent: #6366f1;  /* Primary brand color */
--bg: #f8fafc;      /* Background color */
--text: #1e293b;    /* Text color */
```

### Department Colors
```javascript
const DEPT_COLORS = { 
  IMD: '#4f46e5', 
  DCD: '#f59e0b', 
  TRD: '#d946ef', 
  MED: '#10b981' 
};
```

### Chart Appearance
Adjust chart options in `mkChart()` function:
- Animation duration
- Bar thickness
- Border radius
- Tooltip styling

## Troubleshooting

| Issue | Solution |
|-------|----------|
| "data.xlsx not found" | Ensure file exists in same directory as HTML |
| "No valid rows found" | Check Excel columns match required format |
| Charts not displaying | Verify browser console for errors |
| Export not working | Check if chart data exists before export |
| Focus mode empty | Click chart again after data loads |

## File Structure
```
g-plast-dashboard/
├── index.html          # Main dashboard file
├── data.xlsx          # Your sales data (required)
└── README.md          # Documentation
```

## Future Enhancements
- [ ] Dark mode support
- [ ] Additional chart types (area, line)
- [ ] Date range picker
- [ ] Year-over-year comparisons
- [ ] Profit margin analysis
- [ ] Product category breakdown
- [ ] Email report generation
- [ ] Dashboard save/load states
- [ ] Real-time data refresh

## Support
For issues or questions, please check:
1. Browser console for errors
2. Excel file format requirements
3. Network tab for file loading issues

---
