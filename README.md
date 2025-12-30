# Best School Districts Explorer

An interactive map for exploring top-rated school districts across multiple US states. Filter by Niche grade, home prices, and region.

## Currently Supported States

- 🗽 **New Jersey** - 35 districts (North/Central/South regions)
- 🌽 **Indiana** - 30 districts (Central/North/South regions)

## Features

- **State Switching** - Toggle between supported states with one click
- **Interactive Map** - Leaflet-based map with custom markers color-coded by school grade
- **Grade Filtering** - Filter districts by Niche grade (A+ through B)
- **Price Range Slider** - Filter by median home price ($200K - $1.5M+)
- **Region Filter** - View districts by geographic region within each state
- **Search** - Find districts by town name, ZIP code, or district name
- **Sorting** - Sort results by grade, price, or alphabetically
- **Click to Explore** - Click any result card or map marker for detailed info

## Data

Each district includes:
- Town/City name
- ZIP code
- School district name
- Niche grade (A+ to B)
- Median home price
- County
- Region

**Data Sources:**
- School ratings from [Niche.com](https://www.niche.com) (2024-2025 rankings)
- Home prices from Zillow, Redfin, and local market reports

## Usage

### Option 1: GitHub Pages
Visit the live demo: [your-username.github.io/school-districts-explorer](https://your-username.github.io/school-districts-explorer)

### Option 2: Local
```bash
git clone https://github.com/your-username/school-districts-explorer.git
cd school-districts-explorer
open index.html
```

No build process or dependencies required - it's a single HTML file!

## Adding New States

To add a new state, edit `index.html` and add entries to:

### 1. State Configuration
```javascript
const stateConfigs = {
    // Add your state
    TX: {
        center: [31.9686, -99.9018],  // Lat/Lng center
        zoom: 6,
        regions: ['all', 'north', 'central', 'south', 'west'],
        regionLabels: { all: 'All TX', north: 'North', central: 'Central', south: 'South', west: 'West' }
    }
};
```

### 2. District Data
```javascript
const districtData = {
    TX: [
        {
            zip: "75024",
            town: "Plano",
            district: "Plano ISD",
            grade: "A+",
            price: 550,  // in thousands
            lat: 33.0198,
            lng: -96.6989,
            region: "north",
            county: "Collin"
        },
        // ... more districts
    ]
};
```

### 3. Add State Button
```html
<div class="state-selector">
    <button class="state-btn" data-state="TX">Texas</button>
</div>
```

## Tech Stack

- **HTML/CSS/JavaScript** - Single-file application
- **[Leaflet.js](https://leafletjs.com/)** - Interactive mapping
- **[CartoDB Basemaps](https://carto.com/basemaps/)** - Light map tiles
- **[Source Sans 3](https://fonts.google.com/specimen/Source+Sans+3)** - Typography

## Contributing

Contributions welcome! Ideas:

- [ ] Add more states (Texas, California, etc.)
- [ ] Include additional metrics (test scores, student-teacher ratio)
- [ ] Add commute time estimates to major cities
- [ ] Property tax information
- [ ] Compare districts across states

## License

MIT License - feel free to use, modify, and distribute.

## Disclaimer

This tool is for informational purposes only. School ratings and home prices change frequently. Always verify current information before making decisions.
