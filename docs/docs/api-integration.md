#### `api-integration.md`
```markdown
---
id: api-integration
title: API Integration
---

### Chosen API
We use the [CoinGecko API](https://www.coingecko.com/en/api) because it’s free, reliable, and provides real-time cryptocurrency data.

### Fetching Data
- **Endpoint**: `https://api.coingecko.com/api/v3/coins/markets`
- **Parameters**: 
  - `vs_currency=usd` (prices in USD)
  - `ids=bitcoin,ethereum,binancecoin,cardano,solana` (5 cryptocurrencies)
- **Example Fetch**:
  ```javascript
  async function fetchCryptoPrices() {
    const response = await fetch(
      'https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&ids=bitcoin,ethereum,binancecoin,cardano,solana'
    );
    return response.json();
  }