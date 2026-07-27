# Website Traffic Analysis 📊

A comprehensive Jupyter notebook project that analyzes website traffic patterns, visitor behavior, and performance metrics using Python, Pandas, Plotly, and Matplotlib.

## 📋 Project Overview

This project provides deep insights into:
- **Visitor Behavior**: Total visitors, session duration, bounce rate, pages per session
- **Traffic Sources**: Breakdown of traffic by source (organic, direct, referral, social, paid)
- **Website Performance**: Conversion rates, page load times, user engagement metrics
- **Data Visualizations**: Interactive and static charts for easy interpretation

## 📁 Project Structure

```
Website-Traffic-Analysis/
│
├── dataset/
│   └── website_traffic.csv          # Raw traffic data
│
├── images/                          # Generated visualizations
│   ├── daily_visitors.png
│   ├── bounce_rate.png
│   ├── session_duration.png
│   ├── pages_per_session.png
│   ├── traffic_sources.png
│   └── performance_metrics.png
│
├── Website_Traffic_Analysis.ipynb   # Main analysis notebook
├── README.md                        # This file
├── requirements.txt                 # Python dependencies
└── .gitignore                       # Git ignore rules
```

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook or JupyterLab
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Harsh-Gahlawat/Website-Traffic-Analysis.git
   cd Website-Traffic-Analysis
   ```

2. **Create a virtual environment** (optional but recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

5. **Open and run the notebook**
   - Open `Website_Traffic_Analysis.ipynb`
   - Execute all cells from top to bottom

## 📊 Dataset Requirements

Your CSV file should contain the following columns:

| Column | Type | Description |
|--------|------|-------------|
| `Date` | datetime | Date of the traffic record |
| `Visitors` | integer | Number of unique visitors |
| `Session_Duration` | float | Average session duration in minutes |
| `Bounce_Rate` | float | Bounce rate percentage (0-100) |
| `Pages_Per_Session` | float | Average pages visited per session |
| `Traffic_Source` | string | Source of traffic (optional) |
| `Conversions` | integer | Number of conversions (optional) |
| `Avg_Time_On_Page` | float | Average time spent on page in seconds (optional) |
| `Page_Load_Time` | float | Average page load time in seconds (optional) |

### Sample Data
```
Date,Visitors,Session_Duration,Bounce_Rate,Pages_Per_Session,Traffic_Source
2024-01-01,1250,3.45,42.5,2.3,Organic
2024-01-02,1320,3.67,41.2,2.5,Direct
2024-01-03,980,2.89,48.9,1.8,Referral
```

## 📈 Analysis Sections

### 1. **Data Loading & Exploration** (Steps 4-9)
   - Import required libraries with styled visualization
   - Load and inspect the dataset
   - Check for missing values
   - Generate statistical summary
   - Convert date columns to proper datetime format

### 2. **Data Cleaning** (Section 3)
   - Handle missing values
   - Remove duplicates
   - Verify data integrity

### 3. **Visitor Behavior Analysis** (Section 4)
   - Total visitors count
   - Average session duration
   - Bounce rate analysis
   - Pages per session metrics
   - Daily average visitors

### 4. **Traffic Sources Analysis** (Section 5)
   - Breakdown by traffic source
   - Percentage distribution
   - Source-specific metrics

### 5. **Performance Metrics** (Section 6)
   - Conversion rate calculation
   - Average time on page
   - Page load time analysis
   - Date range overview

### 6. **Visualizations** (Section 7)

**Matplotlib Charts** (Static):
- Daily Visitors Over Time
- Bounce Rate Trend
- Average Session Duration
- Pages Per Session

**Plotly Charts** (Interactive):
- Daily Visitors (Interactive Line Chart)
- Bounce Rate vs Session Duration
- Traffic Distribution (Pie Chart)
- Bounce Rate by Source (Bar Chart)

### 7. **Key Insights & Recommendations** (Section 8)
   - Summary of key metrics
   - Actionable recommendations based on data
   - Performance assessment

## 📊 Key Metrics Calculated

```
Total Visitors              : Sum of all visitors
Average Session Duration    : Mean session time in minutes
Average Bounce Rate         : Mean bounce rate percentage
Average Pages Per Session   : Mean pages per session
Daily Average Visitors      : Mean daily visitors
Overall Conversion Rate     : (Total Conversions / Total Visitors) × 100
```

## 💡 Insights Generated

The notebook automatically generates recommendations based on:

- **Bounce Rate Analysis**: If > 50%, suggests content improvement
- **Session Duration**: If < 2 min, suggests navigation review
- **Pages Per Session**: If < 2, suggests internal linking enhancement
- **General Recommendations**: Continuous monitoring and A/B testing strategies

## 📊 Visualizations

All visualizations are created using:
- **Matplotlib**: Professional static charts with ggplot styling
- **Plotly**: Interactive, hover-enabled charts for better exploration

Charts are displayed inline in the notebook and can be exported as PNG files.

## 🛠️ Technologies Used

- **Python 3.8+**: Programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib**: Static data visualization
- **Plotly**: Interactive visualization
- **Jupyter Notebook**: Interactive computing environment

## 📝 Requirements

See `requirements.txt` for a complete list:
```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
plotly>=5.0.0
jupyter>=1.0.0
```

## 🔄 Workflow

1. **Data Input** → CSV file in `dataset/` folder
2. **Data Processing** → Cleaning and transformation
3. **Analysis** → Statistical calculations
4. **Visualization** → Charts and graphs
5. **Insights** → Recommendations and findings
6. **Export** → Screenshots saved to `images/` folder

## 📌 Usage Example

```python
# Load data
df = pd.read_csv('dataset/website_traffic.csv')

# Convert date
df['Date'] = pd.to_datetime(df['Date'])

# Get insights
total_visitors = df['Visitors'].sum()
avg_bounce_rate = df['Bounce_Rate'].mean()

# Create visualizations
fig = px.line(df, x='Date', y='Visitors', 
              title='Daily Visitors Over Time')
fig.show()
```

## 📖 How to Interpret Results

### Good Metrics
- ✅ Bounce Rate: 20-40% (industry dependent)
- ✅ Session Duration: 2-5 minutes
- ✅ Pages Per Session: 2-3+
- ✅ Conversion Rate: 1-5% (varies by industry)

### Areas for Improvement
- 🔴 High Bounce Rate: Optimize landing pages and CTAs
- 🔴 Low Session Duration: Improve content relevance
- 🔴 Low Pages Per Session: Enhance internal linking
- 🔴 Low Conversion Rate: Test different conversion strategies

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest improvements
- Submit pull requests
- Share insights and use cases

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

**Harsh Gahlawat**
- GitHub: [@Harsh-Gahlawat](https://github.com/Harsh-Gahlawat)
- Email: hjaat6404@gmail.com

## 📚 Resources

- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Matplotlib Documentation](https://matplotlib.org/)
- [Plotly Documentation](https://plotly.com/python/)
- [Jupyter Documentation](https://jupyter.org/)

## ❓ FAQ

**Q: How do I use my own data?**
A: Replace `dataset/website_traffic.csv` with your CSV file that has the required columns.

**Q: Can I modify the visualizations?**
A: Yes! The notebook is fully customizable. Adjust colors, titles, and chart types as needed.

**Q: How often should I run this analysis?**
A: Run it weekly or monthly to track trends and identify patterns over time.

**Q: What if my data has different column names?**
A: Update the column references in the notebook to match your data structure.

## 🚀 Next Steps

1. ✅ Run the notebook with your data
2. ✅ Generate visualizations
3. ✅ Export graphs to `images/` folder
4. ✅ Share insights with stakeholders
5. ✅ Implement recommendations
6. ✅ Schedule regular analysis

## 📞 Support

For questions or issues:
- Open a GitHub issue
- Contact: hjaat6404@gmail.com
- Check the FAQ section above

---

**Last Updated**: July 2026  
**Version**: 1.0.0  
**Status**: ✅ Production Ready
