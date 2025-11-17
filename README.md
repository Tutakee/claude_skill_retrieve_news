# Your Amazing New Skills! 🎉

I've created TWO powerful skills for you:

## 1. 🗞️ Tagesschau News Retrieval Skill

Automatically fetches the latest German news from the official Tagesschau API.

### What it does:
- Retrieves news from the last 24 hours (or any custom time window)
- Filters by German federal states (Bayern, Berlin, Hamburg, etc.)
- Provides both JSON and human-readable text formats
- Highlights breaking news with 🚨 indicators
- Respects API rate limits (60 requests/hour)

### Perfect for:
- "What's the latest German news?"
- "Show me news from Bayern"
- "Any breaking news right now?"
- "Give me headlines from the last 6 hours"

### Key Features:
✅ Time-based filtering (any number of hours)
✅ Regional filtering (all 16 German states)
✅ Breaking news detection
✅ Both JSON and formatted text output
✅ Full API documentation included

---

## 2. 📊 Data Visualization Wizard Skill

Transforms any dataset into beautiful, professional visualizations with intelligent chart selection.

### What it does:
- Analyzes datasets automatically (CSV, Excel, JSON)
- Generates comprehensive data quality reports
- Creates 8 types of publication-quality charts
- Provides insights on correlations, outliers, and patterns
- Uses professional seaborn styling (300 DPI)

### Perfect for:
- "Visualize this data for me"
- "Create a scatter plot of age vs income"
- "Analyze this dataset"
- "Show me trends in my sales data"
- "What insights are in this CSV?"

### Supported Chart Types:
1. **Scatter plots** - correlations between variables
2. **Line charts** - time series and trends
3. **Bar charts** - category comparisons
4. **Histograms** - distributions
5. **Box plots** - group comparisons with outliers
6. **Count plots** - category frequencies
7. **Heatmaps** - categorical relationships
8. **Correlation matrices** - numeric relationships

### Key Features:
✅ Automatic data analysis with insights
✅ Smart chart type suggestions
✅ Publication-quality output (300 DPI)
✅ Outlier detection
✅ Data quality assessment
✅ Multiple visualization formats
✅ Comprehensive best practices guide

---

## How to Use These Skills

1. **Upload the .skill files** to your Claude environment through the skills menu
2. **Just ask naturally** - Claude will automatically use the right skill:
   - "What's happening in Germany?" → Tagesschau skill activates
   - "Plot this data" → Data Viz Wizard activates
3. **Get professional results** - Both skills include robust scripts and documentation

## Technical Details

### Tagesschau News Skill includes:
- `fetch_news.py` - Main retrieval script
- Comprehensive API reference documentation
- Full region code mapping
- Error handling and rate limit management

### Data Viz Wizard includes:
- `analyze_data.py` - Dataset analysis and profiling
- `create_visualization.py` - Chart generation
- `visualization_guide.md` - Best practices reference
- Support for pandas, matplotlib, seaborn

## Files You're Getting

1. `tagesschau-news.skill` - Ready to install
2. `data-viz-wizard.skill` - Ready to install
3. This README explaining everything

Both skills were built following best practices from the skill-creator documentation and are production-ready!

Enjoy your new superpowers! 🚀
