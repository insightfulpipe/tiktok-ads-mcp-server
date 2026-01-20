# TikTok Ads MCP Server

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/tiktok-ads)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect TikTok Ads to AI assistants for automated analytics and campaign optimization.**

The TikTok Ads MCP server brings TikTok advertising data to Claude, ChatGPT, Cursor, and other AI assistants. Analyze campaign performance, optimize ad spend, and get AI-powered insights for your TikTok marketing.

![TikTok Ads MCP Server](https://insightfulpipe.com/images/tiktok-icon.svg)

## MCP Server URL

```
https://tiktok-ads.insightfulmcp.com/
```

## What is TikTok Ads MCP?

TikTok Ads MCP is a **remote Model Context Protocol server** that enables AI assistants to access and analyze your TikTok For Business advertising data. With this MCP integration you can:

- Query TikTok ad performance using natural language
- Analyze video ad engagement and conversion metrics
- Get AI recommendations for creative optimization
- Monitor CPM, CPC, and ROAS across campaigns
- Access detailed campaign, ad group, and ad metadata

## Installation

### Claude

1. Copy the MCP Server URL: `https://tiktok-ads.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** on the connector to start authorization
6. Click **Authorize access** in the browser to complete the connection

### ChatGPT

1. Copy the MCP Server URL: `https://tiktok-ads.insightfulmcp.com/`
2. Open ChatGPT Settings → **Connections**
3. Click **Add Connection** and paste the URL
4. Authorize with your InsightfulPipe account

### Claude Code

```bash
claude mcp add tiktok-ads https://tiktok-ads.insightfulmcp.com/
```

### Cursor

1. Open Cursor Settings → **MCP Servers**
2. Add new server with URL: `https://tiktok-ads.insightfulmcp.com/`
3. Authorize the connection

## Available Actions

| Action | Description |
|--------|-------------|
| `integrated_report_basic` | Primary BASIC reporting endpoint. Supports advertiser, campaign, ad group, and ad level views. TikTok enforces a maximum of four dimensions per request. |
| `ads_metadata` | Returns full ad entity metadata for the specified advertiser |
| `adgroups_metadata` | Returns ad group configuration including targeting, bidding, and schedule settings |
| `campaigns_metadata` | Returns campaign level settings including objective, budget, and schedule |
| `advertisers_metadata` | Returns Business Center advertiser account details (accepts advertiser_id or advertiser_ids list) |

## Usage Examples

### Campaign Performance

```
"How are my TikTok ad campaigns performing this week?"
```

### Video Creative Analysis

```
"Which video ads have the highest completion rate?"
```

### Audience Insights

```
"What demographics are converting best on my TikTok ads?"
```

### Ad Group Analysis

```
"Show me the targeting settings for my top performing ad groups"
```

### Optimization Recommendations

```
"Which TikTok ad groups should I increase budget for?"
```

## Supported TikTok Ad Features

- **In-Feed Ads** - Native video ads in the For You feed
- **TopView Ads** - Premium placement on app open
- **Spark Ads** - Boosted organic content
- **Collection Ads** - Product catalog ads
- **Lead Generation** - In-app lead forms
- **App Install Campaigns** - Mobile app promotion

## Supported Metrics

| Metric | Description |
|--------|-------------|
| Video Views | Total video ad views |
| View Rate | Percentage of impressions that resulted in views |
| 6s View Rate | Users who watched 6+ seconds |
| Completion Rate | Users who watched the full video |
| CTR | Click-through rate |
| CPC | Cost per click |
| CPM | Cost per 1,000 impressions |
| Conversions | TikTok Pixel conversions |
| ROAS | Return on ad spend |

## Why TikTok Ads MCP?

### For TikTok Marketers
- **Real-time insights** - Query live campaign data
- **Creative optimization** - Understand what resonates
- **Trend identification** - Stay ahead on TikTok

### For Gen-Z Focused Brands
- **Audience understanding** - Deep demographic insights
- **Engagement analysis** - Beyond clicks and impressions
- **Content strategy** - Data-driven creative decisions

### For Performance Marketers
- **ROAS tracking** - Full conversion attribution
- **Budget optimization** - AI-powered recommendations
- **Cross-platform comparison** - Compare TikTok vs other channels

## Security

- **TikTok Marketing Partner** - Official API access
- **OAuth 2.0** - Secure authentication
- **Read-only mode** - Safe analytics access
- **Data encryption** - Enterprise-grade security

## Related MCP Servers

- [Facebook Ads MCP](https://insightfulpipe.com/mcp-servers/facebook-ads) - Meta advertising
- [Google Ads MCP](https://insightfulpipe.com/mcp-servers/google-ads) - Google advertising
- [YouTube MCP](https://insightfulpipe.com/mcp-servers/youtube) - YouTube analytics

## Resources

- [Documentation](https://insightfulpipe.com/docs/tiktok-ads)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blogs)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **Email**: support@insightfulpipe.com

## License

MIT License - see [LICENSE](LICENSE) for details.
