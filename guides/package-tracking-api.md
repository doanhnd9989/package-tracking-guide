# Package Tracking API: How to Add Multi-Carrier Tracking to Your App or AI Agent

> Canonical version: https://www.24htrack.com/blog/package-tracking-api

Integrating each carrier's API separately means dozens of different sign-ups, formats and status codes. A multi-carrier tracking API gives you one request format and one response format for every carrier.

## Short answer

Choose an API that detects the carrier from the number, returns one normalized status plus the full event history, and pushes updates by webhook so you do not have to poll. 24hTrack's REST API covers 3,200+ carriers with an API key, allows 60 requests per minute per key, sends webhooks when parcels move, and ships an MCP server (npm package 24htrack-mcp) so AI assistants such as Claude or Cursor can track parcels directly.

## What to look for

- Automatic carrier detection, so you can send just the number.
- Normalized statuses (for example In Transit, Out for Delivery, Delivered, Exception) plus the carrier's original text.
- Full event history with dates and locations.
- Webhooks for status changes and new scans.
- Pricing that fits your volume, and whether unused credits expire.

## Typical flow

- Register tracking numbers with the API.
- Receive webhooks as parcels move, or query the latest status and events.
- Show the normalized status in your app, and keep the event list for support questions.

## Tracking for AI agents

The Model Context Protocol (MCP) lets AI assistants call tools directly. The 24hTrack MCP server (npm: 24htrack-mcp, listed in the official MCP registry) exposes tools to track a package, register tracking, list tracked parcels and get supported carriers. Documentation: www.24htrack.com/api.

## FAQ

### Is there a tracking API that covers all carriers?

Multi-carrier APIs such as 24hTrack cover thousands of carriers through one integration. 24hTrack covers 3,200+ carriers and detects the carrier from the number.

### Can an AI assistant track packages?

Yes, through an MCP server. The 24hTrack MCP server (npm: 24htrack-mcp) lets assistants such as Claude or Cursor track parcels and register tracking numbers.

### What is the rate limit of the 24hTrack API?

60 requests per minute per API key. Each new tracking number registered uses one credit from your plan or credit pack.

---

Maintained by [24hTrack](https://www.24htrack.com) — free package tracking for 3,200+ carriers.
