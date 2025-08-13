# Agricultural Market Pulse Dashboard

A beautiful, responsive web application for analyzing agricultural market data with interactive charts and data visualization.

## 🌟 Features

- **Interactive Charts**: Dynamic bar charts with React/Recharts integration and SVG fallbacks
- **Real-time Data**: Analysis of market messages, crop data, geography, and keywords
- **Responsive Design**: Mobile-friendly interface built with Tailwind CSS
- **Dark Theme**: Modern dark UI with excellent contrast and readability
- **Data Export**: Download complete dataset as JSON
- **Offline Support**: Works without internet connection using built-in SVG charts

## 🚀 Live Demo

Visit the live application: [https://araceaeofcol.github.io/Centro-Aceros/](https://araceaeofcol.github.io/Centro-Aceros/)

## 📊 Data Overview

The dashboard displays analysis of **470 market messages** from **April 15, 2021** to **June 17, 2025**, featuring:

- Top 20 crops (Citrus, Avocado, Banana, Grapes, etc.)
- Top 12 geographies (Peru, Spain, Italy, South Africa, etc.)
- Top 13 keywords (price, harvest, supply, demand, etc.)
- Interactive data tables with filtering capabilities

## 🛠️ GitHub Pages Deployment

### Automatic Deployment (Recommended)

The repository is configured for automatic deployment to GitHub Pages:

1. **Enable GitHub Pages** in repository settings:
   - Go to repository Settings → Pages
   - Source: "Deploy from a branch"
   - Branch: Select your main branch (usually `main` or `master`)
   - Folder: `/ (root)`
   - Click "Save"

2. **Access your site**: Your site will be available at:
   ```
   https://araceaeofcol.github.io/Centro-Aceros/
   ```

### Manual Deployment Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/araceaeofcol/Centro-Aceros.git
   cd Centro-Aceros
   ```

2. **Verify files**:
   ```bash
   ls -la
   # Should show: index.html, README.md, .github/ (if workflow exists)
   ```

3. **Test locally** (optional):
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Then visit: http://localhost:8000
   ```

4. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Deploy to GitHub Pages"
   git push origin main
   ```

### 🔧 Technical Details

- **Entry Point**: `index.html` (GitHub Pages standard)
- **Dependencies**: All loaded from CDNs (no build process required)
- **Compatibility**: Works in all modern browsers
- **Performance**: Optimized with lazy loading and efficient rendering

### 📂 File Structure

```
Centro-Aceros/
├── index.html          # Main application file
├── README.md          # This documentation
└── .github/           # GitHub Actions workflows (optional)
    └── workflows/
        └── deploy.yml # Automated deployment workflow
```

### 🎨 Customization

The application can be customized by modifying the data constants in `index.html`:

- `META`: Update message count and date range
- `TOP_CROPS`: Modify crop data and counts
- `TOP_GEOS`: Update geography information
- `TOP_KEYWORDS`: Change keyword analysis
- `TOP_PAIRS_*`: Update relationship data

### 🐛 Troubleshooting

**Site not loading?**
- Verify GitHub Pages is enabled in repository settings
- Check that `index.html` exists in the root directory
- Ensure the repository is public (for free GitHub Pages)

**Charts not displaying?**
- The app includes fallback SVG charts for offline use
- Modern browsers required for full React/Recharts functionality
- Check browser console for any errors

**Need HTTPS?**
- GitHub Pages automatically provides HTTPS
- Custom domains can be configured in repository settings

### 📞 Support

For issues or questions about deployment, please open an issue in this repository.

---

**Built with ❤️ using modern web technologies**