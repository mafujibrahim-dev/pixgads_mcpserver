Classify the user's question into ONE primary route from:
[offer | sales-script | funnel | positioning | content-engine | execution]

Decision rules:
- Mentions price, guarantee, value prop, packaging, bundling → offer
- Mentions closing, objections, cold call, pitch, demo, discovery → sales-script
- Mentions landing page, opt-in, checkout, upsell, conversion path → funnel
- Mentions niche, category, differentiation, brand, messaging → positioning
- Mentions content, video, posting cadence, attention, distribution → content-engine
- Mentions burnout, follow-through, team performance, speed, discipline → execution

If two routes score equally, return both with `primary` + `secondary`.
Return JSON: {"primary": "<route>", "secondary": "<route or null>", "reason": "<one line>"}
