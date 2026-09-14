# TikTok Ads MCP Server by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/tiktok-ads)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect TikTok Ads to AI assistants for automated analytics and campaign optimization.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — The TikTok Ads MCP server brings TikTok advertising data to Claude, ChatGPT, Cursor, and other AI assistants. Analyze campaign performance, optimize ad spend, and get AI-powered insights for your TikTok marketing.

[![Explore All MCP Servers](https://img.shields.io/badge/Explore_All-MCP_Servers-blue?style=for-the-badge)](https://insightfulpipe.com/mcp-servers)

![TikTok Ads MCP Server](images/tiktok-icon.svg)

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

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://tiktok-ads.insightfulmcp.com/`
3. Authorize with your InsightfulPipe account

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http tiktok-ads https://tiktok-ads.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "tiktok-ads": {
      "url": "https://tiktok-ads.insightfulmcp.com/"
    }
  }
}
```

Then authorize the connection when Cursor prompts you.

## Available Actions

124 actions: 15 read, 109 write.

### Read Actions (15)

| Action | Description |
|--------|-------------|
| `adgroups_metadata` | Returns ad group configuration including targeting, bidding, and schedule settings |
| `ads_metadata` | Returns full ad entity metadata for the specified advertiser |
| `advertisers_metadata` | Returns Business Center advertiser account details (accepts advertiser_id or advertiser_ids list) |
| `campaign_gmv_max_info` | Returns the full configuration of one GMV Max campaign, including its store_id |
| `campaign_gmv_max_session_get` | Returns the details of up to 20 max delivery or creative boost sessions |
| `campaign_gmv_max_session_list` | Lists the max delivery and creative boost sessions inside a Product GMV Max campaign |
| `campaigns_metadata` | Returns campaign level settings including objective, budget, and schedule |
| `gmv_max_campaigns` | Lists GMV Max campaigns |
| `gmv_max_report` | GMV Max campaign performance (cost, orders, gross revenue, ROI, product/video/LIVE breakdowns) |
| `gmv_max_store_list` | Lists the TikTok Shops linked to the advertiser |
| `integrated_report_basic` | Primary BASIC reporting endpoint |
| `tool_bid_recommend` | Get bid recommendations for an ad group based on targeting and objective |
| `tool_targeting_category_recommend` | Get recommended targeting categories based on advertiser vertical |
| `tool_targeting_info` | Get detailed targeting info (location names, ISP info, etc.) |
| `tool_targeting_search` | Search for targeting options by keyword (geo locations, zip codes, etc.) |

### Write Actions (109)

<details>
<summary>Show all 109 write actions</summary>

| Action | Description |
|--------|-------------|
| `ad_create` | Create a new ad (created in DISABLE status for safety) |
| `ad_image_upload` | Upload an image for use in ad creatives |
| `ad_status_update` | Enable, disable, or delete ads in batch |
| `ad_update` | Update an existing ad's creative or settings |
| `ad_video_upload` | Upload a video for use in ad creatives |
| `adgroup_create` | Create a new ad group (created in DISABLE status for safety) |
| `adgroup_status_update` | Enable, disable, or delete ad groups in batch |
| `adgroup_update` | Update an existing ad group's settings |
| `advertiser_update` | Update advertiser account settings (company name, address, etc.) |
| `app_create` | Register a mobile app for ad tracking and optimization |
| `app_update` | Update a registered mobile app's settings |
| `bc_advertiser_create` | Create a new advertiser under a Business Center |
| `bc_asset_admin_delete` | Remove admin permissions for an asset |
| `bc_asset_assign` | Assign assets (ad accounts, pixels, etc.) to BC members or partners |
| `bc_asset_group_create` | Create an asset group in the Business Center |
| `bc_asset_group_delete` | Delete an asset group |
| `bc_asset_group_update` | Update an asset group |
| `bc_asset_unassign` | Unassign assets from BC members or partners |
| `bc_billing_group_create` | Create a billing group in the Business Center |
| `bc_billing_group_update` | Update a billing group |
| `bc_image_upload` | Upload an image to the Business Center asset library |
| `bc_member_delete` | Remove a member from the Business Center |
| `bc_member_invite` | Invite a member to the Business Center |
| `bc_member_update` | Update a Business Center member's role |
| `bc_partner_add` | Add a partner Business Center |
| `bc_partner_asset_delete` | Remove asset sharing with a partner |
| `bc_partner_delete` | Remove a partner Business Center |
| `bc_pixel_link_update` | Update pixel link settings in the Business Center |
| `bc_pixel_transfer` | Transfer pixel ownership between advertisers |
| `bc_transfer` | Transfer funds between Business Center and advertiser accounts |
| `blockedword_create` | Create blocked words for comment filtering |
| `blockedword_delete` | Delete blocked words |
| `blockedword_task_create` | Create a bulk blocked word management task |
| `blockedword_update` | Update blocked words for comment filtering |
| `campaign_create` | Create a new campaign (created in DISABLE status for safety) |
| `campaign_gmv_max_create` | Create a GMV Max campaign for TikTok Shop (created in DISABLE status for safety) |
| `campaign_gmv_max_session_create` | Create a GMV Max session campaign (created in DISABLE status for safety) |
| `campaign_gmv_max_session_delete` | Delete a GMV Max session campaign |
| `campaign_gmv_max_session_update` | Update a GMV Max session campaign |
| `campaign_gmv_max_update` | Update a GMV Max campaign |
| `campaign_status_update` | Enable, disable, or delete campaigns in batch |
| `campaign_update` | Update an existing campaign's settings (name, budget, etc.) |
| `catalog_capitalize` | Capitalize catalog product titles |
| `catalog_create` | Create a product catalog |
| `catalog_delete` | Delete a product catalog |
| `catalog_eventsource_bind` | Bind an event source (pixel/app) to a catalog |
| `catalog_eventsource_unbind` | Unbind an event source from a catalog |
| `catalog_feed_create` | Create a product feed for a catalog |
| `catalog_feed_delete` | Delete a product feed |
| `catalog_feed_update` | Update a product feed |
| `catalog_product_delete` | Delete products from a catalog |
| `catalog_product_file` | Upload a product file to a catalog |
| `catalog_set_delete` | Delete a product set from a catalog |
| `catalog_set_update` | Update a product set in a catalog |
| `catalog_update` | Update a product catalog's settings |
| `catalog_video_delete` | Delete a video from a catalog |
| `comment_delete` | Delete comments on ads |
| `comment_post` | Post a reply to a comment on an ad |
| `comment_status_update` | Hide or unhide comments on ads |
| `comment_task_create` | Create a bulk comment management task |
| `creative_asset_delete` | Delete creative assets (images/videos) |
| `creative_asset_share` | Share creative assets with other advertisers |
| `creative_image_edit` | Edit a creative image (crop, resize, etc.) |
| `creative_portfolio_create` | Create a creative portfolio (instant page, etc.) |
| `creative_shareable_link_create` | Create a shareable link for creative preview |
| `creative_smart_text_generate` | Generate smart text suggestions for ad creatives |
| `custom_audience_apply` | Apply a custom audience to ad groups |
| `custom_audience_create` | Create a custom audience from customer file or engagement data |
| `custom_audience_delete` | Delete custom audiences |
| `custom_audience_file_upload` | Upload a customer file for custom audience creation |
| `custom_audience_lookalike_create` | Create a lookalike audience based on an existing custom audience |
| `custom_audience_lookalike_update` | Update a lookalike audience |
| `custom_audience_rule_create` | Create a rule-based custom audience |
| `custom_audience_share` | Share a custom audience with other advertisers |
| `custom_audience_share_cancel` | Cancel sharing of a custom audience |
| `custom_audience_update` | Update an existing custom audience |
| `gmv_max_exclusive_authorization_create` | Create exclusive authorization for GMV Max campaigns |
| `identity_create` | Create a legacy Custom Identity (CUSTOMIZED_USER) where TikTok still allows it |
| `offline_create` | Create an offline event set for offline conversion tracking |
| `offline_delete` | Delete an offline event set |
| `offline_update` | Update an offline event set |
| `optimizer_rule_batch_bind` | Bind automated rules to entities in batch |
| `optimizer_rule_create` | Create an automated optimization rule |
| `optimizer_rule_update` | Update an automated optimization rule |
| `pangle_block_list_update` | Update the Pangle block list for the advertiser |
| `pixel_batch` | Send pixel events in batch (server-to-server conversion tracking) |
| `pixel_create` | Create a TikTok pixel for conversion tracking |
| `pixel_event_create` | Create a pixel event for tracking specific conversions |
| `pixel_event_delete` | Delete pixel events |
| `pixel_event_update` | Update a pixel event |
| `pixel_track` | Send a single pixel event (server-to-server conversion tracking) |
| `pixel_update` | Update a TikTok pixel's settings |
| `playable_delete` | Delete a playable ad creative |
| `playable_save` | Save a playable ad creative after upload |
| `playable_upload` | Upload a playable ad creative |
| `saved_audience_create` | Create a saved audience with predefined targeting |
| `saved_audience_delete` | Delete saved audiences |
| `smart_plus_ad_appeal` | Appeal a rejected Smart+ ad |
| `smart_plus_ad_create` | Create a Smart+ ad (created in DISABLE status for safety) |
| `smart_plus_ad_material_status_update` | Update material status for Smart+ ads |
| `smart_plus_ad_status_update` | Enable, disable, or delete Smart+ ads in batch |
| `smart_plus_ad_update` | Update a Smart+ ad |
| `smart_plus_adgroup_create` | Create a Smart+ ad group (created in DISABLE status for safety) |
| `smart_plus_adgroup_status_update` | Enable, disable, or delete Smart+ ad groups in batch |
| `smart_plus_adgroup_update` | Update a Smart+ ad group |
| `smart_plus_campaign_create` | Create a Smart+ automated campaign (created in DISABLE status for safety) |
| `smart_plus_campaign_status_update` | Enable, disable, or delete Smart+ campaigns in batch |
| `smart_plus_campaign_update` | Update a Smart+ campaign's settings |
| `term_confirm` | Confirm TikTok terms of service |

</details>

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
- **Budget optimization** - AI-powered recommendations
- **Cross-platform comparison** - Compare TikTok vs other channels

## Security

- **Official TikTok API for Business** - Direct integration with TikTok's API
- **OAuth 2.0** - Secure authentication
- **Data encryption** - Secure transmission

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers for marketing and analytics.

### Advertising MCP Servers
- [Facebook Ads MCP](https://insightfulpipe.com/mcp-servers/facebook-ads) - Meta advertising
- [Google Ads MCP](https://insightfulpipe.com/mcp-servers/google-ads) - Google advertising
- [LinkedIn Ads MCP](https://insightfulpipe.com/mcp-servers/linkedin-ads) - B2B advertising
- [Snapchat Ads MCP](https://insightfulpipe.com/mcp-servers/snapchat-ads) - Snapchat advertising
- [Pinterest Ads MCP](https://insightfulpipe.com/mcp-servers/pinterest-ads) - Pinterest advertising

### Video & Social MCP Servers
- [YouTube MCP](https://insightfulpipe.com/mcp-servers/youtube) - YouTube analytics
- [Instagram MCP](https://insightfulpipe.com/mcp-servers/instagram) - Instagram analytics

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-tiktok-ads)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
