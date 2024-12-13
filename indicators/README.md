# 🌐 Trading Sessions Indicator  

This Pine Script displays trading sessions directly on your TradingView chart by plotting visual session boxes with high and low labels for better analysis of market dynamics during key time periods.  

---

## 🌟 Key Features  

- **Session Boxes**: Visualize trading sessions (e.g., US and London) on the chart using shaded boxes.  
- **High and Low Labels**: Automatically mark the high and low prices for each session with easy-to-read labels.  
- **Custom Session Logic**: Easily adapt to different sessions and trading hours.  

---

## 📊 Sessions Plotted  

- **USA (New York)**:  
  - Open: 9:30 AM (EST)  
  - Close: 4:00 PM (EST)  
  - Box Color: Orange (Transparent)  

- **UK (London)**:  
  - Open: 8:00 AM (GMT)  
  - Close: 4:30 PM (GMT)  
  - Box Color: Green (Transparent)  

---

## 🛠️ How It Works  

1. **Session Boxes**:  
   - Each session is represented as a shaded rectangle on the chart.  
   - The box spans the session's opening and closing times.  

2. **High and Low Tracking**:  
   - During a session, the script tracks the highest and lowest price.  
   - At session close, it marks the high and low prices with labeled markers.  

3. **Customization**:  
   - Add or modify sessions by changing the start and end timestamps in the code.  

---

## 🔧 How to Use  

1. **Copy and Paste**:  
   - Copy the provided Pine Script code.  
   - Open TradingView, go to the **Pine Editor**, and paste the script.  

2. **Add to Chart**:  
   - Click on **Add to Chart** to visualize the trading sessions.  

3. **Customize**:  
   - Update the `timestamp` values for your desired trading sessions.  

---

## 📂 Code Overview  

### Main Components  

1. **`plot_box` Function**  
   - Handles session visualization and logic:  
     - Creates session boxes.  
     - Tracks session highs and lows.  
     - Resets session data after each session.  

2. **Session Definitions**  
   - **US Session**: `us_start` and `us_end`.  
   - **London Session**: `london_start` and `london_end`.  

### Example Visualization  
| Element              | Description                | Example Color      |  
|-----------------------|----------------------------|--------------------|  
| **USA Session Box**   | New York trading hours     | Transparent Orange |  
| **UK Session Box**    | London trading hours       | Transparent Green  |  
| **High/Low Markers**  | Session-specific highs/lows| Green & Red        |  

---

## 🛠️ Customization  

- **Add New Sessions**:  
  Add new sessions by defining `timestamp` variables for start and end times.  

Example:  
```pinescript  
tokyo_start = timestamp("Asia/Tokyo", year, month, dayofmonth, 9, 00)  
tokyo_end = timestamp("Asia/Tokyo", year, month, dayofmonth, 15, 00)  
plot_box("Tokyo", tokyo_start, tokyo_end, color.new(color.blue, 90))  