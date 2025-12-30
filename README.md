# NJ School Districts Explorer

An interactive map for exploring New Jersey school districts by Niche grade, home prices, and region.

![Screenshot](screenshot.png)

## Features

- **Interactive Map** - Leaflet-based map with custom markers color-coded by school grade
- **Grade Filtering** - Filter districts by Niche grade (A+ through B)
- **Price Range Slider** - Filter by median home price ($400K - $1.5M+)
- **Region Filter** - View districts by North, Central, or South NJ
- **Search** - Find districts by town name, ZIP code, or district name
- **Sorting** - Sort results by grade, price, or alphabetically
- **Click to Explore** - Click any result card or map marker for detailed info

## Data

The map includes 35 school districts with the following information:
- Town/City name
- ZIP code
- School district name
- Niche grade (A+ to B)
- Median home price
- County
- Region (North/Central/South NJ)

**Data Sources:**
- School ratings from [Niche.com](https://www.niche.com/k12/search/best-school-districts/s/new-jersey/) (2024-2025 rankings)
- Home prices from Zillow, Redfin, and local market reports

## Usage

### Option 1: GitHub Pages
Simply visit the live demo: [your-username.github.io/nj-school-districts-map](https://your-username.github.io/nj-school-districts-map)

### Option 2: Local
1. Clone the repository
2. Open `index.html` in your browser

```bash
git clone https://github.com/your-username/nj-school-districts-map.git
cd nj-school-districts-map
open index.html  # macOS
# or
start index.html  # Windows
```

No build process or dependencies required - it's a single HTML file!

## Tech Stack

- **HTML/CSS/JavaScript** - Single-file application
- **[Leaflet.js](https://leafletjs.com/)** - Interactive mapping
- **[CartoDB Basemaps](https://carto.com/basemaps/)** - Light map tiles
- **[Source Sans 3](https://fonts.google.com/specimen/Source+Sans+3)** - Typography

## Customization

### Adding Districts

Edit the `schoolDistricts` array in `index.html`:

```javascript
{
  zip: "07XXX",
  town: "Town Name",
  district: "District Name",
  grade: "A+",  // A+, A, A-, B+, or B
  price: 750,   // in thousands (750 = $750K)
  lat: 40.XXXX,
  lng: -74.XXXX,
  region: "north",  // north, central, or south
  county: "County"
}
```

### Changing Colors

Modify the CSS variables in the `:root` selector:

```css
:root {
  --accent: #2563eb;        /* Primary accent color */
  --grade-aplus: #059669;   /* A+ grade color */
  --grade-a: #10b981;       /* A grade color */
  /* ... */
}
```

## License

MIT License - feel free to use, modify, and distribute.

## Contributing

Contributions welcome! Please feel free to submit a Pull Request. Ideas for improvement:

- [ ] Add more districts
- [ ] Include additional data (test scores, student-teacher ratio, etc.)
- [ ] Add commute time estimates to NYC
- [ ] Property tax information
- [ ] Historical price trends

## Disclaimer

This tool is for informational purposes only. School ratings and home prices change frequently. Always verify current information before making decisions. The creator is not affiliated with Niche, Zillow, or any school district.
