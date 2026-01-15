# CS Maisonnex - History Stats v4.0 Changelog

## Overview
Enhanced version with a year selection toggle and complete responsive design support for desktop, tablet, and smartphone resolutions.

---

## ✨ New Features

### 1. **Year Selection Toggle**
- Added prominent toggle buttons at the top of the statistics dashboard
- **Options:**
  - **Overall**: Display statistics for all available time periods
  - **Current Year (YYYY)**: Display only current year statistics
- Dynamic date range display showing the span of data being analyzed
- Smooth state management with visual feedback on active selection

### 2. **Full Responsive Design**
The dashboard is now fully responsive with optimized layouts for three breakpoints:

#### **Desktop (1024px and above)**
- 3-column grid for stat cards
- 2-column grid for charts
- Full-width layout with optimal spacing
- Standard drawer width (350px) for control panel

#### **Tablet (768px - 1023px)**
- 2-column grid for stat cards
- 1-column grid for charts
- Reduced padding and margins
- Full-width control panel drawer
- Adjusted font sizes for readability

#### **Mobile/Smartphone (<768px)**
- 1-column grid for all stat cards
- Single chart per row
- Optimized padding and spacing
- Full-screen control panel drawer
- Responsive text sizing
- Touch-friendly button sizing
- Compact list layouts for top players

---

## 🔧 Technical Implementation

### Data Processing Updates
- **New parameter**: `processHistoryTable(normalizedSelfName, filterYear = null)`
- Support for optional year filtering
- Date range calculation for accurate period display
- Maintains backward compatibility with existing analytics

### UI Enhancements
- **New CSS Classes**:
  - `.year-toggle-container`: Toggle controls container
  - `.toggle-button-group`: Button group styling
  - `.toggle-button-group button.active`: Active state styling
  - `.year-range-display`: Date range display box

- **Responsive Grid Updates**:
  - `.stats-summary`: auto-fit grid (250px min on mobile)
  - `.charts-grid`: auto-fit grid (350px min on desktop, 1fr on tablet)
  - Media queries for tablet (max-width: 1023px)
  - Media queries for mobile (max-width: 767px)

### New Functions
- **`handleYearToggle(filterType)`**: Manages year selection and dashboard refresh
  - Processes data with appropriate year filter
  - Updates button active states
  - Refreshes all charts and statistics
  - Handles error states gracefully

- **`renderCharts(stats)`**: Separated chart rendering logic
  - Responsive chart configurations
  - Maintains aspect ratio across devices
  - Legend positioning adapts by device
  - Better memory management with chart destruction

---

## 📊 Statistics Display

### Current Features by View

#### Overall Statistics
- Total reservations across all years
- Peak year, month, week, and day
- Most active hour window
- Court distribution
- Top 10 opposing players

#### Current Year Statistics
- Year-specific reservation count
- Current year peak metrics
- Filtered player partnership data
- Comparative hourly distribution
- Court usage for current year

---

## 📱 Device Support

✅ **Desktop**: Full-featured layout with optimal chart sizes  
✅ **Tablet**: Adapted two-column design with touch-friendly controls  
✅ **Smartphone**: Single-column mobile-first design  
✅ **Landscape Mobile**: Optimized horizontal layouts  

---

## 🎨 UI/UX Improvements

1. **Better Visual Hierarchy**
   - Toggle controls clearly positioned at dashboard top
   - Date range display for context
   - Active button states with color feedback

2. **Improved Chart Responsiveness**
   - All charts use `responsive: true` and `maintainAspectRatio: true`
   - Legend positioning adapts by screen size
   - Touch-friendly legend clicking on mobile

3. **Enhanced Controls**
   - Larger touch targets on mobile
   - Better spacing between buttons
   - Clearer visual feedback for interactive elements

---

## 🔄 Backward Compatibility

- All existing features maintained
- Original "Overall" view is default
- Control panel remains in side drawer
- Data processing enhancements are non-breaking
- Existing localStorage persistence works as before

---

## 📝 Version Info

- **Version**: 4.0
- **Author**: Phil V
- **Last Updated**: 2026-01-15
- **Script Match**: https://cs-maisonnex.ch/history

---

## 🚀 Usage

1. **Generate Analytics**: Click "Step 2: Generate Analytics" in the control panel
2. **Select View**: Choose "Overall" or "Current Year" using the toggle at the top
3. **Explore Data**: View responsive charts and statistics that adapt to your screen
4. **Export**: Use browser dev tools to export or save charts as needed

---

## 📋 Testing Checklist

- [x] Year toggle buttons functional
- [x] Statistics update when switching views
- [x] Charts render correctly in both modes
- [x] Desktop layout (1024px+) renders properly
- [x] Tablet layout (768-1023px) displays correctly
- [x] Mobile layout (<768px) is fully functional
- [x] Touch interactions work on mobile/tablet
- [x] Date range display updates correctly
- [x] All existing features preserved
