# Your Amazing New Skills! 🎉

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

## Files You're Getting

1. `tagesschau-news.skill` - Ready to install
3. This README explaining everything

The skill was built following best practices from the skill-creator documentation and is production-ready!

Enjoy your new superpowers! 🚀
