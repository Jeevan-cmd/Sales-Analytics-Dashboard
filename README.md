# DataViz Pro - Advanced Data Analysis Platform

A modern, responsive web application for data analysis and visualization built with React, TypeScript, and Plotly.

## Features

### 📊 Comprehensive Data Analysis
- **Multi-format file support**: CSV, Excel (.xlsx, .xls), and text files
- **Automatic data cleaning**: Handles missing values and type conversion
- **Real-time KPI calculations**: Sum, count, averages, and statistical insights
- **Smart column detection**: Automatically identifies numeric, categorical, datetime, and text columns

### 📈 Interactive Visualizations
- **Dynamic bar charts** for categorical data with top N categories
- **Time series line charts** for trend analysis
- **Interactive features**: Hover tooltips, zoom, pan, and click interactions
- **Responsive charts** that adapt to different screen sizes

### 🔍 Advanced Filtering
- **Multi-column filtering** for categorical and datetime columns
- **Date range selection** for time-based filtering
- **Real-time filter application** with instant results
- **Filter persistence** during analysis sessions

### 💾 Data Export
- **CSV export functionality** for filtered datasets
- **Preserve data integrity** during export
- **Timestamped file names** for easy organization

### 🎨 Modern UI/UX
- **Beautiful, responsive design** with gradient themes
- **Smooth animations** using Framer Motion
- **Glass morphism effects** for modern aesthetics
- **Drag-and-drop file upload** with visual feedback
- **Mobile-first design** optimized for all devices

## Technology Stack

- **Frontend Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and building
- **Styling**: Tailwind CSS with custom design system
- **Charts**: Plotly.js for interactive visualizations
- **Animations**: Framer Motion for smooth transitions
- **File Processing**: PapaParse (CSV) and SheetJS (Excel)
- **Data Export**: FileSaver.js for CSV downloads

## Installation & Setup

### Prerequisites
- Node.js 16 or higher
- npm or yarn package manager

### Local Development

1. **Clone and install dependencies**:
   ```bash
   npm install
   ```

2. **Start the development server**:
   ```bash
   npm run dev
   ```

3. **Open your browser** and navigate to `http://localhost:5173`

### Building for Production

```bash
npm run build
```

The built files will be in the `dist` directory.

## Deployment

### Local Deployment
The application can be served locally using:
```bash
npm run preview
```

### Heroku Deployment

1. **Create a Heroku app**:
   ```bash
   heroku create your-app-name
   ```

2. **Add buildpack**:
   ```bash
   heroku buildpacks:set heroku/nodejs
   ```

3. **Deploy**:
   ```bash
   git push heroku main
   ```

4. **Configure build settings** in `package.json`:
   ```json
   {
     "scripts": {
       "start": "npm run preview",
       "build": "vite build",
       "heroku-postbuild": "npm run build"
     }
   }
   ```

## Usage Guide

### 1. File Upload
- Drag and drop files or click to browse
- Supported formats: CSV, Excel (.xlsx, .xls), text files
- Maximum file size: 50MB
- Files are automatically validated and parsed

### 2. Data Analysis
- View comprehensive KPIs and statistics
- Explore automatically generated insights
- Identify patterns in your data

### 3. Interactive Charts
- Bar charts show top categories for categorical columns
- Line charts display trends for time-series data
- Use chart controls for zooming, panning, and detailed exploration

### 4. Data Filtering
- Click the "Filters" button to open the filter panel
- Apply categorical filters by selecting specific values
- Set date ranges for time-based filtering
- View real-time updates as filters are applied

### 5. Data Export
- Export filtered results as CSV files
- Files include timestamps for easy organization
- Maintains data integrity during export

## File Structure

```
src/
├── components/           # React components
│   ├── FileUpload.tsx   # File upload with drag-and-drop
│   ├── KPIDisplay.tsx   # Key performance indicators
│   ├── Charts.tsx       # Interactive Plotly charts
│   ├── FilterPanel.tsx  # Data filtering interface
│   ├── DataTable.tsx    # Data display with pagination
│   ├── ErrorMessage.tsx # Error handling component
│   └── LoadingSpinner.tsx # Loading states
├── utils/               # Utility functions
│   ├── dataProcessor.ts # Data cleaning and analysis
│   └── fileParser.ts    # File parsing for multiple formats
├── types/               # TypeScript type definitions
│   └── data.ts          # Data model interfaces
├── App.tsx              # Main application component
├── main.tsx             # Application entry point
└── index.css            # Global styles and Tailwind imports
```

## Performance Optimizations

- **Code splitting** with dynamic imports
- **Optimized bundle size** with tree shaking
- **Efficient re-rendering** with React.memo and useMemo
- **Lazy loading** for large datasets
- **Memory management** for file processing

## Browser Compatibility

- Chrome 88+
- Firefox 85+
- Safari 14+
- Edge 88+

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

MIT License - see LICENSE file for details.

## Support

For issues and feature requests, please create an issue in the repository.