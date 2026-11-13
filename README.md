# Brush Pack

Free tools a UK painter and decorator's AI assistant uses on the job: paint litres and tins, wallpaper rolls, lead paint safe working, an exterior weather and drying check by postcode, prep checklists and job time estimates.

**Endpoint:** `https://brush-pack.nerolabs.workers.dev/mcp` (MCP, Streamable HTTP)
**Sign-in:** None. No account, no key and no sign-in: add the address and use it.
**How to connect:** https://brush-pack.nerolabs.workers.dev/docs
**Privacy:** https://brush-pack.nerolabs.workers.dev/privacy
**Support:** founder@neroengine.com

## Tools

| Tool | What it does |
|---|---|
| `list_capabilities` | What Brush Pack can do. Lists Brush Pack's tools, surfaces, paint types and what it deliberately does not do. |
| `paint_quantity` | Paint litres and tins. Works out paint for a room (walls, ceiling, woodwork from length, width, height, doors and windows), an exterior (perimeter x height plus gables, less openings) or a custom list of areas. |
| `wallpaper_rolls` | Wallpaper rolls. Rolls of wallpaper for a room or feature wall from wall widths (or room length and width), height, roll width and length (default 10.05 x 0.53 m), pattern repeat and match (free, straight, half drop). |
| `lead_paint_risk` | Lead paint risk and safe working. Judges how likely old paint is to contain lead from the build year, surfaces, paint condition and any test result, checks the planned removal methods (dry sanding, blowlamps and dry scraping are refused; wet abrading, chemical strippers... |
| `exterior_weather_check` | Exterior painting weather and drying check. For a UK postcode (or latitude and longitude) and dates from today up to 8 days ahead, fetches the hourly forecast (MET Norway) and checks each working hour against typical limits for the paint type: minimum temperature, humidity, 3 C... |
| `prep_checklist` | Prep and paint system checklist. How to prepare a surface and which paint system goes on it: checks, prep steps, system (primer, undercoat, top coats) and what to avoid, for new_plaster, previously_painted_walls, bare_softwood, mdf, previously_painted_wood, exterior_wood,... |
| `job_estimate` | Job time and quote estimate. Hours and days on site for a decorating job from rooms (same sizes as paint_quantity, with walls, ceiling and woodwork coats, new_plaster for mist coats) and extra tasks (strip_wallpaper_m2, hang_wallpaper_rolls,... |
| `trade_profile` | Check the decorator's business details. Checks the decorator's own business details (Nero Trade Profile v1: trading name, Companies House number, trade body and number such as PDA or TrustMark, postcode, contact) and returns them cleaned, with a stable `nero_trade_ref` computed... |

Every tool carries a plain title and the read-only, destructive and open-world hints, so your AI app can ask before anything that changes data.

## Connect

- **Claude (web or desktop):** Settings, Connectors, Add custom connector, paste the endpoint.
- **ChatGPT:** Settings, Apps and connectors, Advanced settings, switch on Developer mode, then Create, paste the endpoint, No authentication.
- **Claude Code:** `claude mcp add --transport http brush-pack https://brush-pack.nerolabs.workers.dev/mcp`
- **Cursor, VS Code, Windsurf and others:**

```json
{ "mcpServers": { "brush-pack": { "type": "http", "url": "https://brush-pack.nerolabs.workers.dev/mcp" } } }
```

## Try asking

- "How many tins of emulsion for a 4 by 3.5 metre living room with 2.4 metre ceilings, two coats?"
- "Can I paint the front of a house in LS1 4AP with masonry paint this week? Which days are dry enough?"
- "The house was built in 1955 and I need to sand the old window frames. Is lead paint a risk and what do I do?"

## Good to know

- Built for UK painters and decorators. Every answer shows its working and sources and lists what the trade must check. The trade doing the work stays responsible for it.
- Free forever: no sign-up, no key, no daily cap, no paid plan.

## Privacy

What is kept, what is never kept, and how to get data deleted: https://brush-pack.nerolabs.workers.dev/privacy. Usage counts log the tool name, time, AI app name, country and a one-way scrambled caller code; never your questions, the answers or IP addresses.

This repository holds the listing only (README and server.json). The server runs at the endpoint above.

Built by Nero Labs (Nero Engine Group Ltd, UK).
