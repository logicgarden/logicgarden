# Hi, I'm Caity 🌱

I design systems that hold up under real-world behavior.

I think of systems as ecosystems more than machines: structured environments built for adaptation, observability, and growth that lasts. My instinct is architecture first. I find the layer where a problem actually lives, then build the structure that lets the rest of the system stay simple.

## A few systems that show how I think

**The Hidden Join: routing without relational support.**
A multi-location dermatology group needed patient feedback routed by the provider seen and the location of the visit, together. The platform's grouping logic could only map one field to one value.
I went a layer down, into a calculated-fields area beneath the sanctioned tooling, and fused the two into a single composite key. That turned a two-field problem into a one-field lookup the platform could read.
The workflow was usable at the start of the contract, long before the platform could support the relationship on its own.

**Three Systems, One Contact Record: when persistent state broke attribution.**
Retail, finance, and web events all wrote to a single shared contact record, and context from one interaction kept carrying over into the next. A brand-level survey could be sent using a name pulled from an unrelated interaction.
I moved state from the contact level to the interaction level. Every event now sends a full payload and explicitly clears the fields that don't apply, so the record reflects only the moment it belongs to.
Reporting started matching what customers had actually experienced. The data was never wrong; a value just outlived the interaction that produced it, and nothing could tell a current value from a leftover one.

**Narrative Chemistry: an analytics system I built end to end.**
A normalized database, an ingestion pipeline, and a public REST API with interactive docs.
It runs on a governance contract that defines when automation pauses and what constitutes a destructive action, with a layered source-of-truth hierarchy to resolve conflicts between systems.
The API is live and inspectable at https://api.caity.me/docs.

## Where the work lives

**The Logic Garden.** My systems writing and full project breakdowns: [caity.me](https://www.caity.me)

**Live API and interactive docs.** https://api.caity.me/docs

Most of my code lives in private repositories while it's in flight. The writeups above are the architecture; I'm happy to walk through any of it.
