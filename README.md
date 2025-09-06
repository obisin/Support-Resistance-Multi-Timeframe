# Support/Resistance Multi-Timeframe (S/R MTF)

A multi-timeframe support and resistance indicator that identifies and visualizes key price levels across multiple timeframes simultaneously. This indicator consolidates pivot points from different timeframes to create dynamic support and resistance zones with strength-based visualization.

## KEY FEATURES

### Multi-Timeframe Analysis
• 5 Configurable Timeframes: Analyze support/resistance levels from up to 5 different timeframes  
• Default Setup: 15m, 1H, 6H, 12H timeframes (Daily optional)  
• Smart Consolidation: Automatically merges nearby levels from different timeframes into stronger zones

### Dynamic Level Strength
• Strength-Based Coloring: Levels are colored from green (weak) to red (strongest) based on confluence  
• Adaptive Line Width: Stronger levels display with thicker lines for immediate visual recognition  
• Volume Weighting: Optional volume-based weighting for enhanced level significance

### Level Management
• Level Status Tracking: Distinguishes between untested, respected, and broken levels  
• Broken Level Visualization: Recently broken levels shown with reduced opacity  
• Nearest Level Highlighting: Automatically highlights the closest levels to current price

### Visualization
• Labeling: Displays price values and strength indicators on levels  
• Information Table: Real-time table showing nearest levels with distance calculations  
• Customizable Display: Extensive visual customization options

## HOW IT WORKS

### Pivot Detection
The indicator uses Pine Script's ta.pivothigh() and ta.pivotlow() functions to identify significant price turning points across multiple timeframes. These pivots form the foundation of support and resistance levels.

### Intelligent Price Rounding
More intelligent step sizing based on price magnitude ensures cleaner, more relevant support and resistance lines. The algorithm automatically adjusts rounding precision based on the asset's price range - from 0.0001 for sub-dollar assets to dynamic scaling for higher-priced instruments. This creates better visual clarity and more meaningful level groupings.

### Level Consolidation
When multiple pivots from different timeframes occur near each other (within the merge threshold), they are consolidated into a single, stronger level. This creates more reliable support/resistance zones rather than cluttered individual lines.

### Strength Calculation
Level strength is determined by:  
• Count: Number of times the level has been tested  
• Timeframe Confluence: How many timeframes contribute to the level  
• Volume Weight: Optional volume-based enhancement for level significance

### Status Classification
• Untested (Semi-transparent): Level hasn't been significantly challenged recently  
• Respected (Full opacity): Level has recently held and price reversed  
• Broken (Reduced opacity): Level has been clearly breached

## CONFIGURATION GUIDE

### General Settings
• Bars to Analyze: Number of historical bars to examine per timeframe  
• Pivot Lookback: Period for pivot detection (10 default, range 5-20)  
• Merge Threshold: Percentage range for consolidating nearby levels (0.75% default)  
• Timeframe Selection Configure up to 5 timeframes with individual enable/disable toggles

### Visual Customization
• Minimum Line Strength: Filter out weak levels (3 default)  
• Highlight Nearest: Emphasize closest levels in yellow  
• Line Width Range: Minimum line thickness (3 default)

### Advanced Features
• Volume Weighting: Factor volume into level strength calculations  
• Broken Level Display: Show recently breached levels with transparency  
• Information Table: Display nearest levels with distance metrics

## Interpretation Guidelines

1. Strongest Levels (Red/Purple): Most reliable for major reversals
2. Medium Strength (Blue/Orange): Good for intraday trading decisions
3. Weak Levels (Green/Aqua): Consider as minor support/resistance
