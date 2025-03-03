#### `state-management.md`
```markdown
---
id: state-management
title: State Management
---

### Chosen Approach: React Query
We opted for [React Query](https://tanstack.com/query) because:
- It simplifies data fetching and caching.
- It provides built-in loading and error states.
- It syncs server state efficiently.

### Implementation
```javascript
import { useQuery } from '@tanstack/react-query';

function CryptoDashboard() {
  const { data, refetch, isLoading } = useQuery({
    queryKey: ['cryptoPrices'],
    queryFn: fetchCryptoPrices,
  });

  return (
    <div>
      {isLoading ? <p>Loading...</p> : <CryptoList data={data} />}
      <button onClick={refetch}>Refresh</button>
    </div>
  );
}