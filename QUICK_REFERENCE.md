# 🚀 Quick Reference - Your Two New Skills

## 📊 Data Visualization Wizard
**File:** `data-viz-wizard.skill`

### One-Line Summary
Turn any dataset into beautiful charts with automatic analysis and smart chart selection.

### Quick Commands
```bash
# Analyze data
python3 scripts/analyze_data.py data.csv --format text

# Create scatter plot
python3 scripts/create_visualization.py data.csv scatter plot.png '{"x": "col1", "y": "col2"}'

# Correlation matrix
python3 scripts/create_visualization.py data.csv correlation corr.png
```

### Chart Types
scatter | bar | line | histogram | box | count | heatmap | correlation

### Supported Files
CSV | Excel (.xlsx, .xls) | JSON

---

## 📰 Tagesschau News
**File:** `tagesschau-news.skill`

### One-Line Summary
Fetch German news from Tagesschau with full audit logging for compliance.

### Quick Commands
```bash
# Latest 24h news
python3 scripts/fetch_news.py latest --format text

# Category filter
python3 scripts/fetch_news.py filter wirtschaft --format json

# Regional (Berlin)
python3 scripts/fetch_news.py regions 3 --format markdown

# Search
python3 scripts/fetch_news.py search "your query" --format text
```

### Categories (Ressort)
inland | ausland | wirtschaft | sport | video | investigativ | wissen

### Regions (1-16)
1=Baden-Württemberg | 2=Bayern | 3=Berlin | 10=NRW | etc.

### Output Formats
text | json | markdown

### Key Feature
✅ **Automatic audit logging** - Every API call logged with timestamp and results!

---

## 📝 Remember

### Data Viz
- Always analyze data first
- Move outputs to `/mnt/user-data/outputs/`
- Read `references/visualization_guide.md` for best practices

### Tagesschau  
- Max 60 requests/hour (rate limit)
- Check `tagesschau_audit.log` for audit trail
- Private use only (no redistribution)
- Move outputs to `/mnt/user-data/outputs/`

---

## 🎯 When to Use Each

**Data Visualization Wizard** when user:
- Has a dataset to visualize
- Wants to "create a chart" or "graph this data"
- Needs data analysis or insights
- Asks "what's in this data?"

**Tagesschau News** when user:
- Wants German news
- Asks for "latest Tagesschau" or "German headlines"
- Needs specific categories or regions
- Wants audit trail of news retrieval

---

**Both skills are installed and ready to use!** 🎉
