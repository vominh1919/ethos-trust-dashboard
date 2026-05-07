# Ethos Trust Dashboard

A sleek, dark-themed dashboard for exploring reputation and trust on the [Ethos Network](https://ethos.network).

## Features

- **User Lookup** — Search by wallet address, Twitter handle, or Ethos profile ID
- **Trust Score** — Animated ring gauge showing credibility score (0-5)
- **Activity Feed** — Browse all user activities (reviews, vouches, slashes, votes, replies)
- **Reviews** — View reviews with sentiment badges (positive/negative/neutral)
- **Vouches** — See who vouched for the user and their comments
- **AI Summary** — LLM-powered activity summary via Ethos LLM API
- **System Stats** — Live network-wide statistics (users, reviews, vouches, activities)
- **Dark Neon Theme** — Eye-friendly dark UI with green accent glow
- **Responsive** — Works on mobile, tablet, and desktop

## Tech Stack

- Pure HTML/CSS/JS — zero dependencies, single file
- [Ethos Network API v2](https://developers.ethos.network/) — all public endpoints, no auth required

## API Endpoints Used

| Endpoint | Purpose |
|----------|---------|
| `GET /user/{userkey}` | User profile info |
| `GET /score/{userkey}` | Trust/credibility score |
| `GET /activities/userkey` | Activity feed |
| `GET /reviews/of/{userkey}` | Reviews about user |
| `GET /vouches/of/{userkey}` | Vouches for user |
| `GET /llm/activity-summary` | AI-generated summary |
| `GET /stats/general` | Network-wide stats |

## Userkey Formats

The dashboard auto-detects input format:
- `0x...` → Ethereum address
- `@handle` or `handle` → Twitter username
- `123` → Profile ID
- `profileId:123`, `address:0x...`, `service:x.com:username:handle` — explicit formats

## Usage

Simply open `index.html` in any modern browser. No build step, no server needed.

```bash
# Quick start
open index.html

# Or serve locally
python3 -m http.server 8080 -d ethos-dashboard
```

## License

MIT
