# Hi, I'm Caity 🌱

I design systems that hold up under real-world behavior.

I think of systems less as machines and more as ecosystems: structured environments that support adaptation, observability, and sustainable growth. The work I care about most wasn't optimized into existence. It was cultivated.

My instinct is architecture first. I find the layer where a problem actually lives, then build the structure that lets the rest of the system stay simple.

## A few systems that show how I think

**The Hidden Join — routing without relational support.**
A multi-location dermatology customer needed patient feedback routed by both the provider seen and the location of the visit. The platform's grouping logic could only map one field to one value.
I went a layer down and synthesized a composite key inside a configuration layer beneath the sanctioned tooling, turning a two-field problem into a one-field lookup.
The customer was unblocked from day one of the contract instead of three months in.

**Three Systems, One Contact Record — when persistent state broke attribution.**
Retail, financial, and web events all wrote to a single shared contact record, and context from one interaction kept leaking into the next.
I moved state from the contact level to the interaction level: every event sends a full payload and explicitly clears the fields that don't apply.
Reporting started reflecting what actually happened. The lesson stuck: shared data models don't break because the data is wrong. They break because data doesn't forget.

**Narrative Chemistry — an analytics system I built end to end.**
A normalized database, an ingestion pipeline, and a public REST API with interactive docs, built over about seven weeks.
It runs on a governance contract that defines when automation pauses and what counts as destructive, plus a layered source-of-truth hierarchy for resolving conflicts between systems.
The API is live and inspectable at https://www.caity.me/nchem-api.

## Where the work lives

🌿 **The Logic Garden** — my systems writing and full project breakdowns: [caity.me](https://www.caity.me)
🔗 **Live API + interactive docs:** https://www.caity.me/nchem-api

*Most of my code lives in private repositories while it's in flight. The writeups above are the architecture; happy to walk through any of it.*
