# 📊 Excelerate - Desktop Spreadsheet Assistant

A powerful, no-code desktop application for data analysis and visualization. Excelerate allows non-technical users to upload CSV and Excel files, perform data cleaning, create pivot tables, and generate beautiful charts with an intuitive web-based interface.

## ✨ Features

### 📁 File Upload & Support
- **Multiple Formats**: Support for CSV, Excel (.xlsx, .xls) files
- **Drag & Drop**: Easy file upload with drag-and-drop interface
- **File Validation**: Automatic file type detection and validation
- **Large File Support**: Efficient handling of large datasets

### 🧹 Data Cleaning
- **Remove Blank Rows/Columns**: Automatically clean empty data
- **Trim Whitespace**: Remove leading/trailing spaces from text data
- **Fill Missing Values**: Multiple strategies (mean, median, mode, custom)
- **Date Standardization**: Automatic date format detection and conversion
- **Data Validation**: Comprehensive data quality checks

### 📊 Pivot Table Builder
- **No-Code Interface**: Create pivot tables without writing formulas
- **Multiple Aggregations**: Sum, count, mean, median, min, max
- **Flexible Layout**: Choose rows, columns, and values
- **Real-time Preview**: See results instantly
- **Export Options**: Save pivot tables as CSV or Excel

### 📈 Chart Generator
- **Multiple Chart Types**:
  - Pie Charts (with donut option)
  - Vertical Bar Charts
  - Horizontal Bar Charts
  - Histograms
  - Line Charts
  - Scatter Plots
- **Interactive Charts**: Built with Plotly for rich interactions
- **Customization**: Titles, colors, and styling options
- **Export as PNG**: High-quality image export

### 💾 Export Options
- **Data Export**: Save cleaned data and pivot tables as CSV or Excel
- **Chart Export**: Export charts as high-resolution PNG files
- **Organized Storage**: Automatic organization in Documents folder
- **File Naming**: Timestamped files for easy identification

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher
- Windows 10/11 (for .exe build)

### Option 1: Run from Source

1. **Clone or download the project**
   ```bash
   git clone <repository-url>
   cd excelerate
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   python -m app.main
   ```

4. **Open in browser**
   - Navigate to `http://127.0.0.1:7860`
   - The application will open automatically in your default browser

### Option 2: Build Standalone Executable

1. **Install PyInstaller**
   ```bash
   pip install pyinstaller
   ```

2. **Build the executable**
   ```bash
   pyinstaller build.spec
   ```

3. **Run the executable**
   - Navigate to `dist/excelerate/`
   - Run `excelerate.exe`

## 📖 Usage Guide

### Getting Started

1. **Upload Your Data**
   - Click "Upload CSV or Excel file" or drag and drop your file
   - Supported formats: `.csv`, `.xlsx`, `.xls`
   - Click "Load File" to process your data

2. **Data Preview**
   - View your data in the interactive table
   - Check data types and missing values
   - Verify data quality before processing

3. **Clean Your Data**
   - Select cleaning options:
     - Remove blank rows/columns
     - Trim whitespace
     - Fill missing values
   - Click "Clean Data" to apply transformations

4. **Create Pivot Tables**
   - Choose row and column fields
   - Select value field and aggregation function
   - Click "Create Pivot Table" to generate results

5. **Generate Charts**
   - Select chart type (pie, bar, histogram, etc.)
   - Choose X and Y axis columns
   - Add a title and click "Create Chart"

6. **Export Results**
   - Export cleaned data as CSV or Excel
   - Save charts as PNG images
   - Files are saved to `Documents/Excelerate_Exports/`

### Advanced Features

#### Data Cleaning Strategies
- **Mean/Median**: For numeric data with missing values
- **Mode**: For categorical data
- **Custom Value**: Specify your own fill value
- **Date Detection**: Automatic date column identification

#### Chart Recommendations
The application suggests appropriate chart types based on your data:
- **Categorical + Numeric**: Bar charts, pie charts
- **Numeric + Numeric**: Scatter plots, line charts
- **Distribution**: Histograms

#### Pivot Table Tips
- Use categorical columns for rows and columns
- Use numeric columns for values
- Choose appropriate aggregation functions
- Add totals for better analysis

## 🏗️ Architecture

```
excelerate/
│
├── app/                 # Main application code
│   ├── __init__.py     # Package initialization
│   ├── main.py         # Entry point and UI
│   ├── logic.py        # Data processing and pivot logic
│   ├── charts.py       # Chart generation
│   └── utils.py        # Helper functions
│
├── assets/             # Sample files and resources
│   └── sample.csv      # Sample data for testing
│
├── requirements.txt    # Python dependencies
├── README.md          # This file
├── .gitignore         # Git ignore rules
└── build.spec         # PyInstaller configuration
```

### Technology Stack
- **Frontend**: Gradio (Python web framework)
- **Data Processing**: Pandas, NumPy
- **Visualization**: Plotly
- **File Handling**: OpenPyXL, XlsxWriter
- **Build Tool**: PyInstaller

## 🔧 Configuration

### Customization Options
- **Export Directory**: Files are saved to `Documents/Excelerate_Exports/`
- **Port**: Default port is 7860 (configurable in `main.py`)
- **Theme**: Uses Gradio's Soft theme (customizable)

### Settings File
Application settings are stored in:
```
Documents/Excelerate_Exports/excelerate_settings.json
```

## 🐛 Troubleshooting

### Common Issues

1. **Port Already in Use**
   - Change the port in `main.py` line 280
   - Or close other applications using port 7860

2. **File Upload Issues**
   - Ensure file is not corrupted
   - Check file format is supported
   - Verify file size is reasonable (< 100MB)

3. **Chart Not Displaying**
   - Check that selected columns exist
   - Ensure data types are appropriate
   - Try different chart types

4. **Export Failures**
   - Check write permissions in Documents folder
   - Ensure sufficient disk space
   - Verify file is not open in another application

### Performance Tips
- For large files (>10MB), consider splitting data
- Use appropriate data types for better performance
- Close unnecessary browser tabs
- Restart application if memory usage is high

## 🤝 Contributing

We welcome contributions! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

### Development Setup
```bash
# Install development dependencies
pip install -r requirements.txt
pip install pytest black flake8

# Run tests
pytest

# Format code
black app/

# Lint code
flake8 app/
```

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- **Gradio** for the excellent web interface framework
- **Pandas** for powerful data manipulation
- **Plotly** for beautiful interactive charts
- **PyInstaller** for creating standalone executables

## 📞 Support

For support and questions:
- Create an issue on GitHub
- Check the troubleshooting section
- Review the documentation

---

**Excelerate** - Making data analysis accessible to everyone! 📊✨ 
