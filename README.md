# ARGUS Intelligence Skill for ClawHub

**AI-native blockchain intelligence & security for AI agents.**

## Quick Start

```bash
# Install via ClawHub
clawhub install argus-intelligence

# Or set endpoint directly
export ARGUS_ENDPOINT="http://34.233.47.6:8080"
```

## What is ARGUS?

ARGUS is a blockchain intelligence agent that provides:

- **Token Analysis** - Rug pull detection, risk scoring ($0.42)
- **Address Risk** - Sanctions, AML, compliance ($0.42)
- **Smart Money Tracking** - Whale movements ($0.42)
- **Prompt Security** - Injection attack detection ($0.10) **NEW!**
- **Free Tier** - 3 queries/day, no payment needed!

## Try It Free

```bash
curl -X POST http://34.233.47.6:8080/api/v1/free/query \
  -H "Content-Type: application/json" \
  -d '{"query": "Is 0x1234... safe?", "agentId": "my-agent"}'
```

## Pricing

| Service | Cost |
|---------|------|
| Free Tier | 3/day FREE |
| Intelligence | $0.42 USDC |
| Prompt Security | $0.10 USDC |
| Watchlist | $0.10/month |

## Links

- **Live API:** http://34.233.47.6:8080
- **Agent Card:** http://34.233.47.6:8080/.well-known/agent.json
- **Full Docs:** See [SKILL.md](./SKILL.md)
- **Website:** https://getfailsafe.com

## Version

**v1.2.0** - Added prompt security, free tier, referrals, watchlist monitoring

---

Built by Failsafe Security Inc.
