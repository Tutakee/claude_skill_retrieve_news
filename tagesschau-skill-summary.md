# 🎉 Tagesschau News Retrieval Skill - Complete!

## What I Built For You

A professional-grade skill for retrieving German news from Tagesschau with comprehensive audit logging capabilities.

## 📦 Packaged Skill

**File:** `tagesschau-news.skill`

This skill is ready to install and use immediately. It includes:

### Core Features

✅ **News Retrieval** - Fetch news from Tagesschau API
- Latest news (time-filtered from 1-48 hours)
- Homepage featured/breaking news
- Category-filtered news (wirtschaft, sport, inland, ausland, etc.)
- Regional news from any of 16 German states
- Full-text search capabilities

✅ **Comprehensive Audit Logging** - Every API interaction is logged
- Timestamp for every action
- Request details (endpoint, parameters)
- Response status (success/failure)
- Item counts retrieved
- Error messages and debugging info
- Perfect for compliance and troubleshooting

✅ **Multiple Output Formats**
- Text - Human-readable console output
- JSON - Structured data for processing
- Markdown - Formatted documents

✅ **Smart Filtering**
- Time-based filtering (e.g., last 24 hours)
- Category filtering (7 categories)
- Regional filtering (16 German states)
- Search functionality

## 📄 What's Included

### 1. Main Script (`fetch_news.py`)
Comprehensive Python script with:
- Full API integration
- Automatic audit logging
- Error handling and timeout management
- Date parsing and filtering
- Multiple output formats
- Rate limit awareness

### 2. API Reference Documentation
Complete guide to Tagesschau API including:
- All endpoints and parameters
- Response structures
- Rate limits (60 requests/hour)
- Legal usage restrictions
- Error handling
- Example requests and responses

### 3. SKILL.md
Detailed usage instructions covering:
- Quick start guide
- All available commands
- Workflow patterns
- Troubleshooting
- Best practices
- Output handling

### 4. Usage Examples Document
Real-world examples showing:
- Common use cases
- Example commands
- Expected outputs
- Pro tips and tricks

## 🚀 How to Use

### Installation
1. Upload the `tagesschau-news.skill` file to Claude
2. The skill will be automatically installed

### Basic Usage Examples

**Get latest 24-hour news:**
```bash
python3 scripts/fetch_news.py latest --format text --output news.txt
```

**Get business news:**
```bash
python3 scripts/fetch_news.py filter wirtschaft --format json --output business.json
```

**Search for topics:**
```bash
python3 scripts/fetch_news.py search "climate change" --format markdown --output climate.md
```

**Get regional news (Berlin):**
```bash
python3 scripts/fetch_news.py regions 3 --format text --output berlin_news.txt
```

### Audit Logging

Every command automatically creates `tagesschau_audit.log` with entries like:

```
2025-11-17 14:30:15 | INFO | SESSION START | Command: latest | Format: text
2025-11-17 14:30:15 | INFO | API REQUEST | Endpoint: /api2u/news/ | Params: None
2025-11-17 14:30:16 | INFO | API SUCCESS | Status: 200 | Items: 45 news items
2025-11-17 14:30:16 | INFO | FILTER | Filtered 12 items from last 24 hours
2025-11-17 14:30:16 | INFO | SESSION END | Success | Total items: 12
```

## ⚠️ Important Notes

### Rate Limits
- **Maximum 60 requests per hour**
- Script logs all requests for monitoring
- Exceeding limit results in 429 errors

### Legal Usage
- ✅ Private, non-commercial use allowed
- ❌ No publication or redistribution
- See: https://tagesschau.de/creativecommons

### Network Requirements
- Requires internet access to www.tagesschau.de
- 30-second timeout on requests

## 🎯 Key Benefits

1. **Audit Trail** - Complete logging of all API interactions for compliance
2. **Flexible** - Multiple commands, formats, and filters
3. **User-Friendly** - Clear output formats and comprehensive documentation
4. **Production-Ready** - Error handling, timeouts, logging all built-in
5. **Well-Documented** - Extensive documentation and examples

## 📚 Documentation Files

1. **tagesschau-usage-examples.md** - Real-world usage examples
2. Inside skill: `SKILL.md` - Complete usage guide
3. Inside skill: `references/api_reference.md` - API documentation

## 🔍 What Makes This Special

Unlike a simple API wrapper, this skill provides:

- **Professional audit logging** for tracking and compliance
- **Intelligent date filtering** to get news from specific time windows
- **Multiple output formats** for different use cases
- **Comprehensive error handling** with detailed logging
- **Complete documentation** at every level
- **Production-ready code** with proper timeout handling and error recovery

## 💪 Use Cases

- **News Monitoring** - Track German news daily
- **Research** - Search and filter news by topic
- **Regional Analysis** - Monitor specific German states
- **Compliance** - Audit logs prove all API usage
- **Data Collection** - JSON output for further analysis
- **Reporting** - Markdown output for documents

## 🎓 Next Steps

1. Install the skill by uploading `tagesschau-news.skill`
2. Review `tagesschau-usage-examples.md` for common patterns
3. Start with simple commands like `fetch_news.py latest`
4. Check audit logs to understand API usage
5. Explore advanced filtering and search options

---

**Both skills are ready to use!** The Tagesschau news skill is packaged and documented with comprehensive audit logging as requested. 🎉
