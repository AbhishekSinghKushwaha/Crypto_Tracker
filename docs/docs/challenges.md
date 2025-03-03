#### `challenges.md`
```markdown
---
id: challenges
title: Challenges & Solutions
---

### Challenge 1: API Rate Limits
- **Issue**: CoinGecko’s free tier has rate limits.
- **Solution**: Implemented caching with React Query (stale time of 60 seconds) to reduce API calls.

### Challenge 2: Responsive Design
- **Issue**: Dashboard looked cluttered on mobile.
- **Solution**: Used CSS Grid and media queries to adjust layout for smaller screens.

### Challenge 3: Search Functionality
- **Issue**: Filtering large datasets was slow.
- **Solution**: Limited initial fetch to 5 coins and filtered locally with JavaScript.