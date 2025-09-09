# 🗺️ Indian State Literacy Map - GeoPandas Visualization Project

A comprehensive **GeoPandas-based choropleth mapping project** that visualizes literacy rates across Indian states with interactive features, statistical analysis, and highlighting of underperforming regions.






***

## 📋 Table of Contents
- [🎯 Features](#-features)
- [🚀 Quick Start](#-quick-start)
- [📁 Project Structure](#-project-structure)
- [📊 Data Sources](#-data-sources)
- [📈 Expected Outputs](#-expected-outputs)
- [🎨 Customization](#-customization)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

***

## 🎯 Features

### Core Visualization Features
- **📍 Choropleth Mapping**: Color-coded states based on literacy percentages
- **🎯 National Average Highlighting**: Red borders around states below national average
- **💡 Interactive Tooltips**: Hover information with state names and exact literacy rates
- **📊 Statistical Dashboard**: Real-time calculation of national averages and extremes
- **🎨 Custom Color Schemes**: Green-to-red gradient for intuitive interpretation

### Technical Features
- **🔄 Dual Rendering**: Both Matplotlib (static) and Plotly (interactive) outputs
- **📱 Responsive Design**: Works across different screen sizes
- **⚡ Performance Optimized**: Efficient data processing and visualization
- **🔧 Modular Code**: Easy to extend and customize
- **📋 Data Validation**: Automatic data quality checks and error handling

***

## 🚀 Quick Start

### Prerequisites
```bash
Python 3.8+
pip (Python package manager)
```

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/Indian-State-Literacy-Map.git
   cd Indian-State-Literacy-Map
   ```

2. **Create virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

### Quick Run
```bash
# Generate static map
python literacy_map.py

# Generate interactive map
python literacy_map.py --interactive

# Generate both maps with analysis
python literacy_map.py --all
```

***

## 📁 Project Structure

```
Indian-State-Literacy-Map/
│
├── 📄 literacy_map.py              # Main script
├── 📊 data/
│   ├── literacy_rates.csv         # Source literacy data
│   └── india_states.geojson       # Geographic boundaries (auto-downloaded)
├── 📈 output/
│   ├── static_literacy_map.png    # Generated static map
│   ├── interactive_map.html       # Generated interactive map
│   └── analysis_report.txt        # Statistical analysis
├── 📚 docs/
│   ├── demo_static.png           # Static map preview
│   └── demo_interactive.gif      # Interactive map demo
├── 🛠️ requirements.txt            # Python dependencies
├── 📖 README.md                   # This file
└── 📜 LICENSE                     # MIT License
```

***

## 📊 Data Sources

### Geographic Data
- **Source**: Indian state boundaries GeoJSON from Data{Meet} community[9][10]
- **Format**: GeoJSON with state polygons and metadata
- **Auto-download**: Script automatically fetches latest boundaries

### Literacy Rate Data
- **Source**: Census 2023-24 compiled from government sources[11][12]
- **Coverage**: All 28 states and 8 union territories
- **Format**: CSV with State and LiteracyRate columns

**Sample Data Format:**
```csv
State,LiteracyRate
Kerala,95.3
Mizoram,98.2
Bihar,61.8
```

***

## 📈 Expected Outputs

### 1. Static Choropleth Map (Matplotlib)
- **File**: `output/static_literacy_map.png`
- **Resolution**: High-DPI (300 DPI) for publication quality
- **Features**: 
  - Color-coded states by literacy percentage
  - Red borders highlighting below-average states
  - Statistical information panel
  - Professional styling with custom colormap

### 2. Interactive Map (Plotly)
- **File**: `output/interactive_map.html`
- **Features**:
  - Hover tooltips with state details
  - Zoom and pan functionality
  - Click interactions
  - Responsive design for different devices

### 3. Statistical Analysis Report
- **File**: `output/analysis_report.txt`
- **Contents**:
  - National literacy average calculation
  - Top 5 and bottom 5 performing states
  - States below national average identification
  - Statistical measures (standard deviation, range)

### Key Insights Generated
Based on the latest data, the analysis reveals:[11]

- **📊 National Average**: Approximately 76.3%
- **🏆 Highest Literacy**: Mizoram (98.2%), Lakshadweep (97.3%), Kerala (95.3%)
- **⚠️ Lowest Literacy**: Bihar (61.8%), Rajasthan (66.1%), Andhra Pradesh (67.0%)
- **📍 Regional Patterns**: Northeastern and southern states generally show higher literacy rates
- **🔍 States Below Average**: Automatically identified and highlighted with red borders

***

## 🎨 Customization

### Using Custom Data
Replace `data/literacy_rates.csv` with any CSV containing:
- `State`: State/region names matching GeoJSON boundaries
- `LiteracyRate`: Numerical values to visualize

### Command Line Options
```bash
# Basic usage
python literacy_map.py

# Custom data file
python literacy_map.py --data custom_literacy.csv

# Save specific outputs
python literacy_map.py --save-static --save-interactive

# Disable below-average highlighting
python literacy_map.py --no-highlight

# Custom threshold for highlighting
python literacy_map.py --threshold 70
```

### Color Scheme Customization
The project supports multiple color palettes:
- **Default**: Green-to-red gradient
- **Education-focused**: Custom academic color scheme
- **Accessibility-friendly**: Color-blind safe palette

***

## 🤝 Contributing

We welcome contributions! Here's how to get started:

### Development Setup
```bash
# Fork and clone the repository
git clone https://github.com/your-username/Indian-State-Literacy-Map.git
cd Indian-State-Literacy-Map

# Create feature branch
git checkout -b feature/amazing-feature

# Install development dependencies
pip install -r requirements-dev.txt

# Run tests
python -m pytest tests/

# Check code style
black literacy_map.py
flake8 literacy_map.py
```

### Contribution Areas
- [ ] Add district-level mapping capability
- [ ] Implement time-series analysis for multiple years
- [ ] Add export functionality for different formats (SVG, PDF)
- [ ] Create web-based dashboard interface
- [ ] Add comparison with other educational metrics
- [ ] Improve mobile responsiveness

### Guidelines
1. **🐛 Bug Reports**: Use GitHub issues with detailed descriptions
2. **✨ Feature Requests**: Propose new features with use cases
3. **📝 Documentation**: Improve README, comments, or docs
4. **🧪 Testing**: Add tests for new functionality
5. **🎨 Code Style**: Follow PEP 8 and use black formatter

***

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

### Data Attribution
- **Geographic boundaries**: Data{Meet} community (Public Domain)
- **Literacy statistics**: Government of India Census data (Open Government License)

***

## 🏷️ Tags & Keywords

`geopandas` -  `choropleth-map` -  `data-visualization` -  `india-literacy` -  `educational-data` -  `python-mapping` -  `statistical-analysis` -  `government-data` -  `census-visualization` -  `interactive-maps`

***

## 📞 Support & Contact

- **🐛 Issues**: https://github.com/SHASHI1401933
- **💬 Discussions**: [GitHub Discussions](https://github.com/your-username/Indian-State-Literacy-Map/discussions)
- **📧 Email**: Shashi_2312res979@iitp.ac.in

***

## 🌟 Acknowledgments

- **Data{Meet}** community for providing open-source India boundary data
- **Government of India** for making census data publicly available
- **GeoPandas** and **Plotly** development teams for excellent visualization libraries
- Contributors and users who help improve this project

***

**⭐ If this project helps you understand Indian literacy patterns better, please star this repository!**

*Made with ❤️ for educational data visualization and evidence-based policy research.*

[1](https://gist.github.com/ramantehlan/602ad8525699486e097092e4158c5bf1)
[2](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
[3](https://stackoverflow.com/questions/23989232/is-there-a-way-to-represent-a-directory-tree-in-a-github-readme-md)
[4](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/)
[5](https://github.com/mhucka/readmine)
[6](https://coding-boot-camp.github.io/full-stack/github/professional-readme-guide/)
[7](https://github.com/RichardLitt/standard-readme)
[8](https://www.makeareadme.com)
[9](https://github.com/Subhash9325/GeoJson-Data-of-Indian-States)
[10](https://github.com/udit-001/india-maps-data)
[11](https://www.jagranjosh.com/general-knowledge/list-of-indian-states-with-highest-and-lowest-literacy-rate-1748938921-1)
[12](https://www.scribd.com/document/804432903/literacy-rate-csv-file-data)
