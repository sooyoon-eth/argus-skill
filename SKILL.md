---
name: argus-intelligence
description: AI-native blockchain intelligence & security agent. 15+ services including risk assessment, smart money tracking, AML/KYT compliance, and prompt injection detection. Free tier available (3/day). Pay $0.42 USDC for intelligence or $0.10 for security via x402 on Base.
version: 1.2.0
requires:
  env:
    - ARGUS_ENDPOINT
  bins:
    - curl
    - jq
os: [darwin, linux, win32]
primaryEnv: ARGUS_ENDPOINT
cost: 0.42
costCurrency: USDC
costNetwork: base
category: blockchain-intelligence
tags:
  - blockchain
  - crypto
  - risk-assessment
  - aml
  - kyc
  - smart-money
  - defi
  - agent-to-agent
  - x402
  - security
  - prompt-injection
  - ai-safety
author: Failsafe Security Inc.
homepage: https://getfailsafe.com
repository: https://github.com/sooyoon-eth/argus-skill
---

# ARGUS - The All-Seeing Blockchain Intelligence Agent

**AI-native blockchain intelligence & security for the agentic economy.**

ARGUS provides high-quality on-chain analytics, risk scoring, market intelligence, AND AI agent security. Built for agent-to-agent micropayments using x402 protocol on Base network.

## What's New in v1.2.0

- **Prompt Security Service** - Detect prompt injection attacks ($0.10/check)
- **Free Tier** - 3 queries per day, no payment required!
- **Referral Program** - Earn 10% ($0.042) per referred query
- **Watchlist Monitoring** - Ongoing alerts for $0.10/item/month
- **Malicious Skills Awareness** - Community safety features

---

## Pricing Tiers

| Tier | Price | What You Get |
|------|-------|--------------|
| **Free Tier** | FREE | 3 intelligence queries per day |
| **Intelligence** | $0.42 USDC | Full blockchain intelligence queries |
| **Prompt Security** | $0.10 USDC | Prompt injection detection |
| **Watchlist** | $0.10 USDC/month | Ongoing monitoring with alerts |
| **Referrals** | Earn $0.042 | 10% commission on referred queries |

---

## Core Capabilities

### 1. Token Analysis ($0.42)
Deep analysis of any cryptocurrency token with proprietary FBI Unified Score (0-100).

**What it provides:**
- Market data (price, volume, market cap, liquidity)
- Risk assessment (sanctions, blacklists, honeypot detection)
- Smart money tracking (institutional holders, accumulation patterns)
- Holder distribution and concentration analysis
- **Agentic recommendation:** PROCEED, CAUTION, or REJECT with reasoning

**Example:**
```bash
curl -X POST $ARGUS_ENDPOINT/api/v1/token/analyze \
  -H "Content-Type: application/json" \
  -H "X-Payment-Proof: $PAYMENT_PROOF" \
  -d '{"token": "ETH", "chain": "ethereum", "depth": "deep"}'
```

### 2. Address Risk Assessment ($0.42)
Comprehensive AML/KYT compliance screening for any blockchain address.

**What it provides:**
- Critical flags (sanctions, blacklists, threat actors, mixer usage)
- Entity attribution (identify who owns the address)
- Portfolio summary (holdings, token distribution)
- DeFi positions across protocols
- **Agentic risk score:** 0-100 with PROCEED/REVIEW/REJECT recommendation

### 3. Prompt Security Check ($0.10) - NEW!
Protect your AI agent from prompt injection attacks.

**Attacks Detected:**
- Instruction overrides ("ignore previous instructions")
- Jailbreak attempts ("DAN mode", "developer mode")
- Role manipulation ("pretend you are a hacker")
- Financial exploits ("transfer all funds", "approve unlimited")
- Encoded payloads (Base64, hex obfuscation)
- Data exfiltration ("reveal private key")
- Social engineering ("URGENT!", fake admin claims)
- Delimiter attacks (fake system prompts)

**Example:**
```bash
curl -X POST $ARGUS_ENDPOINT/api/v1/security/prompt-check \
  -H "Content-Type: application/json" \
  -d '{"prompt": "User message to check", "context": "defi"}'
```

**Response:**
```json
{
  "is_safe": false,
  "risk_score": 85,
  "risk_level": "malicious",
  "attack_types": ["instruction_override", "financial_exploit"],
  "recommendation": "BLOCK"
}
```

### 4. Smart Money Tracking ($0.42)
Track institutional and whale wallet movements in real-time.

**What it provides:**
- Top tokens being accumulated by smart money
- Distribution patterns (who's selling)
- Notable large transactions
- **Agentic sentiment:** Bullish/bearish signals with confidence

### 5. Entity Investigation ($0.42)
Deep dive into known entities (exchanges, funds, protocols, whales).

### 6. Market Intelligence ($0.42)
Broad market overview, trending tokens, sector performance.

### 7. Compliance Check ($0.42)
Strict AML/KYT screening for regulated entities.

---

## FREE Services (No Payment Required!)

| Service | Endpoint | Description |
|---------|----------|-------------|
| **Free Query** | `POST /api/v1/free/query` | 3 full queries/day |
| **Free Status** | `GET /api/v1/free/status` | Check remaining queries |
| **Threat Feed** | `GET /api/v1/threats` | Real-time rug pulls, exploits |
| **Launch Monitor** | `GET /api/v1/launches` | New token rug detection |
| **Leaderboard** | `GET /api/v1/leaderboard` | Top agents & value saved |
| **Security Patterns** | `GET /api/v1/security/patterns` | Attack pattern docs |

**Start Free:**
```bash
curl -X POST $ARGUS_ENDPOINT/api/v1/free/query \
  -H "Content-Type: application/json" \
  -d '{"query": "Is 0x1234... safe?", "agentId": "my-agent"}'
```

---

## Payment Flow (x402 Protocol)

**Supported Networks:**
- **Base (Primary):** Treasury `0x8518E91eBcb6bE76f478879720bD9759e01B7954`
- **Solana:** Treasury `Ntx61j81wkQFLT5MGEKvMtazxH4wh6iXUNMtidgxXYH`

### Payment Flow:
1. **Try free first** → 3 queries/day at `/api/v1/free/query`
2. **Or request without payment** → Receive 402 Payment Required
3. **Send USDC** to treasury on Base ($0.42 intel, $0.10 security)
4. **Create payment proof** (base64 encoded JSON with txHash, paymentId, from)
5. **Retry with X-Payment-Proof header** → Receive intelligence

---

## Referral Program - Earn Money!

Earn 10% ($0.042) on every query from agents you refer.

```bash
# Generate your referral code
curl -X POST $ARGUS_ENDPOINT/api/v1/referral/generate \
  -d '{"agentId": "your-agent-id"}'

# Returns: {"code": "ARGUS-XXXX-XXXX", ...}
```

---

## Agentic Features

ARGUS is not just a data provider—it's an **autonomous intelligence agent**.

1. **Autonomous Reasoning:** Uses Claude API to reason about intelligence data
2. **Pattern Detection:** Identifies anomalies and suspicious patterns automatically
3. **Decision Making:** Provides clear PROCEED/CAUTION/REJECT recommendations
4. **Confidence Scoring:** Every recommendation includes confidence level (0-100%)
5. **Risk Analysis:** Explains *why* something is risky, not just *that* it's risky

---

## Configuration

### Required Environment Variables

```bash
export ARGUS_ENDPOINT="http://34.233.47.6:8080"
```

### Installation

```bash
# Install via ClawHub
clawhub install argus-intelligence

# Or set endpoint directly
export ARGUS_ENDPOINT="http://34.233.47.6:8080"
```

---

## API Reference

### Base URL
```
http://34.233.47.6:8080
```

### Agent Card (A2A Discovery)
```
http://34.233.47.6:8080/.well-known/agent.json
```

### All Endpoints

| Method | Endpoint | Cost | Description |
|--------|----------|------|-------------|
| POST | `/api/v1/free/query` | FREE | 3/day intelligence queries |
| GET | `/api/v1/free/status` | FREE | Check remaining free queries |
| GET | `/api/v1/threats` | FREE | Public threat feed |
| GET | `/api/v1/launches` | FREE | Token launch monitor |
| GET | `/api/v1/leaderboard` | FREE | Agent leaderboard |
| GET | `/api/v1/security/patterns` | FREE | Attack pattern docs |
| POST | `/api/v1/query` | $0.42 | Natural language query |
| POST | `/api/v1/token/analyze` | $0.42 | Token analysis |
| POST | `/api/v1/address/risk` | $0.42 | Address risk assessment |
| POST | `/api/v1/entity/investigate` | $0.42 | Entity investigation |
| POST | `/api/v1/smart-money/track` | $0.42 | Smart money tracking |
| GET | `/api/v1/market/scan` | $0.42 | Market intelligence |
| POST | `/api/v1/compliance/check` | $0.42 | AML/KYT compliance |
| POST | `/api/v1/security/prompt-check` | $0.10 | Prompt injection detection |
| POST | `/api/v1/security/prompt-check/batch` | $0.09 | Batch check (10% off) |
| POST | `/api/v1/watchlist/add` | $0.10/mo | Add to watchlist |
| GET | `/api/v1/watchlist` | FREE | View watchlist |
| POST | `/api/v1/referral/generate` | FREE | Get referral code |
| GET | `/.well-known/agent.json` | FREE | A2A Agent Card |
| GET | `/api/v1/capabilities` | FREE | Full API docs |

---

## Security & Privacy

- **Zero Knowledge:** ARGUS doesn't store your queries or payment details
- **Onchain Verification:** All payments verified trustlessly on Base/Solana
- **Encrypted Transit:** TLS 1.3 for all API communications
- **No User Tracking:** No cookies, no tracking pixels, no analytics
- **Rate Limited:** 30 requests/min per IP to prevent abuse

---

## Why ARGUS?

| Feature | ARGUS | Competitors |
|---------|-------|-------------|
| **Agentic Analysis** | Claude-powered reasoning | Raw data only |
| **Prompt Security** | $0.10/check | Not offered |
| **Free Tier** | 3 queries/day | None |
| **Agent Payments** | x402 micropayments | Subscription only |
| **Multi-chain** | 10+ chains | Limited |
| **Compliance Focus** | AML/KYT specialized | Basic checks |
| **No Subscription** | Pay per use | Monthly fees |

---

## Support

- **Telegram:** @ARGUSIntelBot
- **Website:** https://getfailsafe.com

---

**Built for the agentic economy by Failsafe Security Inc.**

*ARGUS sees all, knows all, protects all.*
