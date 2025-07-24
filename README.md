# 📊 Google Drive File Analysis Tool

A powerful web-based tool for analyzing Google Drive file creation patterns, storage growth, and generating forecasts. Perfect for organizations looking to understand their document storage trends and plan for future capacity needs.

## 🌟 Features

- **📁 Smart Folder Filtering**: Automatically filters files from specific folder hierarchies (including deeply nested folders)
- **📈 Timeline Analysis**: Visualizes file creation patterns over time with monthly and yearly breakdowns
- **🔮 Growth Forecasting**: Generates predictions using both linear and exponential growth models
- **🌳 Folder Tree Visualization**: Shows complete folder structure with file counts
- **📊 Interactive Charts**: Beautiful, responsive charts powered by Chart.js
- **💾 Storage Analysis**: Tracks file sizes and storage growth trends
- **🎯 Real-time Filtering**: Processes large CSV files efficiently in the browser

## 🚀 Live Demo

**[Try the tool here →](https://victorlepri.github.io/gdrive-analyser/)**

## 📋 How to Use

### Step 1: Export Your Google Drive Data with GAM

First, use [GAM (Google Apps Manager)](https://github.com/GAM-team/GAM) to export your Drive data:

```bash
gam user your.email@domain.com print filelist corpora allteamdrives fields id,name,createdTime,modifiedTime,size,mimeType,owners,parents > drive_files.csv
```

### Step 2: Upload and Analyze

1. Open the [analysis tool](https://victorlepri.github.io/gdrive-analyser/)
2. Drag and drop your CSV file into the upload area
3. The tool will automatically:
   - Filter files from your target folders
   - Show detailed statistics and breakdowns
   - Generate interactive charts and forecasts
   - Display folder structure with file counts

### Step 3: Interpret Results

The tool provides:
- **File creation timeline** (monthly/yearly trends)
- **Growth forecasts** for the next 3 years
- **Storage usage** and size analysis
- **Folder breakdown** showing which areas have the most files

## 🛠️ Technical Features

- **Client-side Processing**: All analysis happens in your browser - no data leaves your device
- **Large File Support**: Efficiently handles thousands of files using PapaParse
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Modern Web Technologies**: Built with vanilla JavaScript, Chart.js, and CSS3

## 📊 What You'll Learn

- How many files are created per month/year
- Which folders are growing fastest
- Predicted storage needs for future planning
- File type distribution and patterns
- Team productivity and document creation trends

## 🎯 Perfect For

- **IT Administrators** planning storage capacity
- **Operations Teams** understanding document workflows
- **Business Analysts** tracking team productivity
- **Compliance Teams** monitoring file creation patterns
- **Anyone** curious about their organization's document patterns

## 🔧 Development

### Local Development

```bash
# Clone the repository
git clone https://github.com/victorlepri/gdrive-analyser.git
cd gdrive-analyser

# Serve locally (Python 3)
python -m http.server 8000

# Or use any local server
# Open http://localhost:8000
```

### Technologies Used

- **HTML5/CSS3/JavaScript** - Core web technologies
- **Chart.js** - Beautiful, responsive charts
- **PapaParse** - Fast CSV parsing
- **GitHub Pages** - Free hosting and deployment

## 📁 Repository Structure

```
gdrive-analyser/
├── index.html          # Main application
├── README.md           # This file
├── assets/
│   └── screenshot.png  # Tool screenshot
└── examples/
    └── sample_data.csv # Example CSV format
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch
3. Make your improvements
4. Submit a pull request

### Ideas for Contributions

- Additional chart types (pie charts, heatmaps)
- Export functionality for reports
- More advanced forecasting algorithms
- Custom folder filtering options
- File type analysis features

## 📝 CSV Format Requirements

Your CSV should include these columns:
- `id` - File ID
- `name` - File name
- `createdTime` - Creation timestamp
- `mimeType` - File type
- `size` - File size in bytes
- `parents.0.id` - Parent folder ID

## 🚀 Deployment

This tool is automatically deployed via GitHub Pages. Any push to the `main` branch will update the live version.

## 📜 License

MIT License - Feel free to use this tool for any purpose!

## 💡 Inspiration

Created to solve the challenge of understanding Google Drive usage patterns in organizations using GAM exports. Originally built for contract folder analysis but works with any Drive structure.

---

**Made with ❤️ for better Drive analytics**

[Live Tool](https://victorlepri.github.io/gdrive-analyser/) | [Report Issues](https://github.com/victorlepri/gdrive-analyser/issues) | [Star on GitHub](https://github.com/victorlepri/gdrive-analyser)