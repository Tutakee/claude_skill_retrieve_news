# Tagesschau News Skill - Usage Examples

## 📰 What This Skill Does

Retrieves German news from Tagesschau (ARD's main news service) with comprehensive audit logging for all API interactions. Perfect for tracking German news, monitoring specific topics, or building news feeds.

## 🚀 Quick Examples

### Example 1: Get Today's Headlines
**User request:** "Get me the latest German news from the last 24 hours"

**Claude's action:**
```bash
python3 scripts/fetch_news.py latest 24 --format markdown --output latest_news.md
cp latest_news.md /mnt/user-data/outputs/
cp tagesschau_audit.log /mnt/user-data/outputs/
```

**Result:** Markdown file with all news from past 24 hours + audit log

---

### Example 2: Business News Research
**User request:** "I need all wirtschaft (business) news from Tagesschau"

**Claude's action:**
```bash
python3 scripts/fetch_news.py filter wirtschaft --format json --output business_news.json
cp business_news.json /mnt/user-data/outputs/
cp tagesschau_audit.log /mnt/user-data/outputs/
```

**Result:** JSON file with all business/economics news + audit log

---

### Example 3: Regional News Monitoring
**User request:** "What's the news from Berlin and Bayern?"

**Claude's action:**
```bash
# Berlin = region 3, Bayern = region 2
python3 scripts/fetch_news.py regions 3,2 --format text --output regional_news.txt
cp regional_news.txt /mnt/user-data/outputs/
cp tagesschau_audit.log /mnt/user-data/outputs/
```

**Result:** Text file with news from Berlin and Bavaria + audit log

---

### Example 4: Topic Search
**User request:** "Search Tagesschau for articles about renewable energy"

**Claude's action:**
```bash
python3 scripts/fetch_news.py search "renewable energy" --format markdown --output energy_news.md
cp energy_news.md /mnt/user-data/outputs/
cp tagesschau_audit.log /mnt/user-data/outputs/
```

**Result:** Markdown file with search results + audit log

---

### Example 5: Breaking News
**User request:** "Show me the top stories from Tagesschau homepage"

**Claude's action:**
```bash
python3 scripts/fetch_news.py homepage --format text
```

**Result:** Featured news and breaking stories displayed in console

---

## 📊 Audit Log Features

Every command creates detailed audit entries:

```
2025-11-17 14:30:15 | INFO | SESSION START | Command: latest | Format: text
2025-11-17 14:30:15 | INFO | API REQUEST | Endpoint: /api2u/news/ | Params: None
2025-11-17 14:30:16 | INFO | API SUCCESS | Status: 200 | Items: 45 news items
2025-11-17 14:30:16 | INFO | FILTER | Filtered 12 items from last 24 hours
2025-11-17 14:30:16 | INFO | SESSION END | Success | Total items: 12
```

**Logged information:**
- ✅ Timestamp for every action
- ✅ API endpoints called
- ✅ Request parameters
- ✅ Success/failure status
- ✅ Number of items retrieved
- ✅ Filtering operations
- ✅ Error details (if any)

---

## 🎯 Common Use Cases

### Daily News Briefing
```bash
python3 scripts/fetch_news.py latest 24 --format markdown --output daily_brief.md
```
Get a comprehensive daily news summary

### Category Monitoring
```bash
python3 scripts/fetch_news.py filter sport --format json --output sports.json
```
Track specific news categories (sport, wirtschaft, politik, etc.)

### Geographic Focus
```bash
python3 scripts/fetch_news.py regions 10 --format text --output nrw_news.txt
```
Monitor news from specific German states

### Topic Research
```bash
python3 scripts/fetch_news.py search "climate policy" --format markdown --output research.md
```
Find articles on specific topics

### Recent Breaking News
```bash
python3 scripts/fetch_news.py latest 6 --format text
```
Get very recent news (last 6 hours)

---

## ⚠️ Important Limitations

**Rate Limits:**
- Maximum 60 API requests per hour
- Exceeding this will result in 429 errors
- Monitor with: `grep "API REQUEST" tagesschau_audit.log | wc -l`

**Legal Usage:**
- ✅ Private, non-commercial use only
- ❌ No redistribution or publication
- See: https://tagesschau.de/creativecommons

**Network Requirements:**
- Requires access to www.tagesschau.de
- 30-second timeout on requests

---

## 💡 Pro Tips

1. **Always save audit logs** - They're invaluable for debugging and tracking API usage
2. **Use time filters wisely** - Don't fetch all news when you only need recent
3. **Combine with other tools** - JSON output is perfect for further processing
4. **Check logs for errors** - `grep ERROR tagesschau_audit.log`
5. **Count your requests** - Stay under 60/hour limit

---

## 🔧 Customization Options

### Output Formats
- `--format text` - Human-readable (default)
- `--format json` - Structured data
- `--format markdown` - Formatted documents

### Time Filters
- `latest 6` - Last 6 hours
- `latest 12` - Last 12 hours  
- `latest 24` - Last 24 hours (default)
- `latest 48` - Last 48 hours

### Custom Log Location
```bash
--log /path/to/custom_audit.log
```

### Save to File
```bash
--output filename.txt
```

---

## 📁 File Structure

After installation, the skill contains:

```
tagesschau-news/
├── SKILL.md                      # Main documentation
├── scripts/
│   └── fetch_news.py             # Main retrieval script
└── references/
    └── api_reference.md          # Complete API documentation
```

---

## 🎓 Learning the API

For complete API details, read `references/api_reference.md`:
- All available endpoints
- Response structures
- Parameter options
- Error codes
- Best practices

This is especially useful when you need to understand API responses or troubleshoot issues.
