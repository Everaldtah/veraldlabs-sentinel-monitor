# Veraldlabs Sentinel Monitor

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Three.js](https://img.shields.io/badge/three.js-r128-black?logo=three.js)

A high-fidelity global intelligence and surveillance dashboard featuring real-time 3D globe visualization, multi-source camera feeds, and comprehensive threat analysis.

![Dashboard Preview](https://raw.githubusercontent.com/Everaldtah/veraldlabs-sentinel-monitor/main/docs/preview.png)

## Live Demo

**[View Live Dashboard](https://veraldlabs-sentinel-monitor.vercel.app)**

## Features

### 3D Globe Visualization
- Interactive WebGL globe powered by Three.js
- Real-time event markers with severity-based color coding
- Multiple view modes: Standard, Satellite, Thermal
- Atmospheric glow effects and wireframe overlays
- Click-to-select event interaction
- Auto-rotation with manual controls

### Live Camera Feeds
- Multi-panel camera grid (4 active feeds)
- Status indicators (Online/Alert/Offline)
- Simulated night vision and thermal overlays
- Recording indicators with pulsing animation
- Expandable full-screen view

### Event Monitoring
- Real-time event log with severity filtering
- Event type icons (Earthquake, Conflict, Weather, Vessel, Flight)
- Source attribution (USGS, NATO, AIS)
- Timestamp tracking
- Click-to-select on globe

### System Metrics
- CPU/Memory/Network/Storage monitoring
- Real-time progress bars
- Data throughput visualization
- Satellite link status (24/32 active)

### Threat Analysis
- Global threat level assessment
- Regional activity breakdown
- Critical and High alert counters
- Progress indicators for key metrics

## Tech Stack

- **3D Graphics**: Three.js (r128)
- **Styling**: Custom CSS with CSS Grid
- **Fonts**: JetBrains Mono, Rajdhani
- **Icons**: Custom SVG

## Project Structure

```
veraldlabs-sentinel-monitor/
├── index.html          # Main dashboard (single file)
├── vercel.json         # Vercel deployment config
└── README.md           # Documentation
```

## Getting Started

### Option 1: Direct Open
Simply open `index.html` in any modern web browser.

### Option 2: Local Server
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

### Option 3: Deploy to Vercel
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Performance

- Optimized Three.js rendering
- Efficient CSS Grid layout
- Minimal JavaScript footprint
- 60 FPS animation target

## Customization

### Changing Event Data
Edit the `events` array in the JavaScript section of `index.html`:

```javascript
const events = [
    {
        id: 'evt-001',
        type: 'earthquake',
        severity: 'high',
        title: 'Your Event Title',
        desc: 'Event description',
        coords: { lat: 35.6762, lng: 139.6503 },
        source: 'USGS'
    }
];
```

### Adding Camera Feeds
Edit the `cameraFeeds` array:

```javascript
const cameraFeeds = [
    {
        id: 'cam-001',
        name: 'Camera Name',
        location: 'Location',
        coords: '39.8283°N 98.5795°W',
        status: 'online' // online, alert, offline
    }
];
```

### Theme Colors
Modify CSS variables in the `<style>` section:

```css
:root {
    --bg-primary: #0a0a0f;
    --accent-cyan: #00d4ff;
    --accent-green: #00ff88;
    --accent-amber: #ffaa00;
    --accent-red: #ff4444;
}
```

## API Integration

The dashboard is designed to work with various data sources:

### Real Data Sources (Optional)
- **USGS Earthquake Feed**: Real-time seismic data
- **OpenSky Network**: Live flight tracking
- **AIS Stream**: Vessel tracking
- **NewsAPI**: Breaking news headlines

### Fallback Data
When APIs are unavailable, the dashboard uses realistic simulated data.

## Deployment

### GitHub Pages
1. Push code to GitHub repository
2. Go to Settings > Pages
3. Select source branch (main)
4. Your site will be live at `https://yourusername.github.io/veraldlabs-sentinel-monitor`

### Vercel
1. Connect GitHub repository to Vercel
2. Deploy with zero configuration
3. Auto-deploy on every push

### Netlify
1. Drag and drop the project folder
2. Or connect GitHub repository
3. Deploy instantly

## Security

- No external API calls (all data is local)
- No cookies or tracking
- HTTPS enforcement in production
- Content Security Policy compatible

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Three.js community for 3D graphics
- JetBrains for the Mono font
- Google Fonts for Rajdhani

## Contact

Veraldlabs Team

Project Link: [https://github.com/Everaldtah/veraldlabs-sentinel-monitor](https://github.com/Everaldtah/veraldlabs-sentinel-monitor)

---

Built with by Veraldlabs
