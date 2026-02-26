---
name: throttled
description: Rate limiting library with multiple strategies (fixed window, sliding window, token bucket, leaky bucket, GCRA). Use when implementing API rate limiting, request throttling, or quota management in TypeScript/Node.js projects.
---

# throttled

Full-featured rate limiting for TypeScript/Node.js. Port of Python's throttled-py.

## Setup

```bash
npm install @indiekitai/throttled
```

## CLI Usage

```bash
# Test rate limiter interactively
npx @indiekitai/throttled --strategy fixed-window --rate "10/minute"

# JSON output
npx @indiekitai/throttled --strategy token-bucket --rate "100/hour" --json
```

## Programmatic Usage

```typescript
import { FixedWindow, SlidingWindow, TokenBucket, LeakyBucket, GCRA } from '@indiekitai/throttled';

// Fixed window: 10 requests per minute
const limiter = new FixedWindow({ rate: 10, period: 60_000 });
const result = limiter.allow('user-123');
// { allowed: true, remaining: 9, resetAt: ... }

// Token bucket: burst-friendly
const bucket = new TokenBucket({ rate: 10, period: 60_000, burst: 20 });

// Sliding window: smooth distribution
const sliding = new SlidingWindow({ rate: 100, period: 3600_000 });
```

## Strategies

- **FixedWindow** — Simple time-window counting
- **SlidingWindow** — Weighted window for smoother limits
- **TokenBucket** — Allows bursts up to bucket size
- **LeakyBucket** — Constant drain rate, smooths traffic
- **GCRA** — Generic Cell Rate Algorithm, telco-grade precision
