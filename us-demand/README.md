# Pedestal: US Market Opportunity

A 29-month snapshot of **US demand** across Pedestal's Shopify storefronts (Jun 2024 to
Oct 2026): the 11 European storefronts for the whole period, plus the US store
(us.pedestal.com) from its launch on **23 September 2026**. Before launch there was no
US-localized store and no US-targeted ad spend, yet US visitor sessions were substantial
and growing fast, almost entirely organically.
Bot & AI-agent traffic is flagged out so the headline reflects **real people**.

## Start here
Open **`index.html`** in any browser: it's the one-page summary with the
animated maps, growth chart, top markets, and method notes.

## The numbers (real customers, bots/AI agents removed)
- **US store live 23 September 2026** (us.pedestal.com)
- **213,212** real US visitor sessions over 29 months (182,838 of them in the 27 months before launch)
- **+86% year-over-year** (last 12 months vs the prior 12: ~125,000 vs ~67,200 sessions); a log-linear trend implies ≈71%/yr
- **19,508 real sessions in October 2026**, the first full month with the US store open (US store 9,093 · European storefronts 10,415), roughly double the summer level (Jun 9,222 · Jul 8,920 · Aug 10,350)
- Top states: **California (40.4k) › New York (27.6k) › Texas (18.5k) › Washington › Florida › Illinois**
- Top cities: **New York › Los Angeles › Brooklyn › Chicago › San Jose › Fort Worth › Seattle › Dallas**
- California + New York + Texas ≈ **40%** of US demand

## What's in the box
```
index.html                     One-page opportunity summary (open this)
maps/
  states-by-month.html   Interactive animated state choropleth (also embedded in index.html)
  cities-by-month.html   Interactive animated city bubble map (top metros)
charts/
  overview.html / overview.png     Real humans vs bots/AI agents; growth + top markets
data/
  real-customers_state-by-month.csv   Real-customer sessions by state × month
  real-customers_city-by-month.csv    Real-customer sessions by city × month
  all-traffic_state-by-month.csv      All sessions incl. bots/AI agents (for reference)
  all-traffic_city-by-month.csv       All sessions incl. bots/AI agents (for reference)
```
The maps are interactive and embedded in `index.html`; the charting library loads
from a CDN, so viewing needs an internet connection.

## Method & the bot/AI caveat
- **Source:** Shopify "Sessions by location" report, United States only, monthly:
  the 11 European storefronts (10 consumer stores + B2B) for the whole period and
  the US store from 23 Sep 2026. US visitors still reach the European storefronts
  after launch, so both are counted to keep the series comparable. Figures are
  **website sessions (visits), not orders.**
- **Why filter bots/AI agents:** ~49% of raw "US sessions" originate from cloud
  datacenters: Council Bluffs IA (Google), Ashburn VA (AWS), North Bergen NJ,
  Forest City NC (Meta), Prineville OR. These are search/AI crawlers, on-demand
  AI fetchers (ChatGPT, Perplexity, Google AI) and uptime/monitoring bots. They
  geolocate to the **server**, not a person, so including them would put the
  "market" wherever Amazon/Google/Meta keep their servers (it makes Iowa and New
  Jersey outrank California). They're excluded from the real-customer view and
  preserved in the `all-traffic_*` files.
- **The filter follows the bots.** During 2026 the older hubs went quiet and new
  ones ramped up, mostly Meta's newer datacenter sites. The exclusion list was
  extended in Aug 2026 (Social Circle GA, Gallatin TN, DeKalb IL, Huntsville AL,
  Eagle Mountain UT, all Meta, plus Hillsboro OR, St Louis MO, Columbus OH,
  Springfield NE, Sandston VA) and re-applied to the full series so every month
  is stated on the same basis (this trimmed previously published history by ~3%).
  Nov 2026: Eatonton GA and Los Lunas NM (Meta) added; bot bursts removed from
  two real metros on the European storefronts only, San Jose CA (Aug to Oct 2026)
  and Kansas City MO (Sep 2026), where the extra traffic was spread evenly over
  all 11 stores. US-store sessions from those cities are kept. Earlier months
  moved by fewer than 20 sessions (172,506 to 172,488 for Jun 2024 to Jul 2026).
  New datacenter towns are identified by an even session spread across all 11
  storefronts (real US visitors concentrate heavily on the EN-language stores)
  plus a step-ramp from near zero.
- **AI-driven *human* visits are still counted.** When a person reads a ChatGPT
  or Google-AI answer that cites Pedestal and clicks through, that's a normal
  session at their real location, already in the real-customer numbers.
- Mixed metro/datacenter cities (e.g. Fort Worth TX, Des Moines IA) are kept in
  the real-customer view when the store-mix looks predominantly human; a finer
  user-agent-level split remains a logical next step.

*Prepared June 2026 · updated August 2026 and November 2026 · data through October 2026.*
