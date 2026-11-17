# Hi, I'm Caity 🌱

I design systems that hold up once people start using them.

I think of systems as ecosystems more than machines: structured environments built for adaptation, observability, and growth that lasts. My instinct is architecture first. I find the layer where a problem actually lives, then build the structure that lets the rest of the system stay simple.

## A few systems that show how I think

**The Hidden Join: routing without relational support.**
A multi-location dermatology group needed patient feedback routed by the provider seen and the location of the visit, together. The platform's grouping logic could *only* map one field to one value.
I went a layer down, beneath the sanctioned tooling, into the platform's calculated fields. There I fused the two into a single composite key, which turned a two-field problem into a one-field lookup the platform could read.
The workflow was usable at the start of the contract, long before the platform could support the relationship on its own.

**Three Systems, One Contact Record: when persistent state broke attribution.**
Retail, finance, and web events all wrote to a single shared contact record, and context from one interaction carried over into the next. A brand-level survey could go out with a name pulled from an unrelated interaction.
I moved state from the contact level to the interaction level. Every event now sends a full payload and explicitly clears the fields that don't apply, so the record reflects only the moment it belongs to.
Each value was accurate for the interaction that wrote it. The trouble came when it outlived that interaction, and nothing could tell a current value from a leftover one. Once state moved, reporting matched what customers had actually experienced.

**Narrative Chemistry: an analytics system I designed and built end to end with an AI coding agent.**
It has a normalized database, an ingestion pipeline, and a public REST API with interactive docs.
It runs on a governance contract that defines when automation stops and what counts as a destructive action, which I describe in Executor Mode. A layered source-of-truth hierarchy settles conflicts between systems.

## Where the work lives

**The Logic Garden.** My systems writing and full project breakdowns: [caity.me](https://www.caity.me)

**Live API and interactive docs.** https://api.caity.me/docs

Most of my code lives in private repositories while it's in progress. The writeups on caity.me cover the architecture, and I'm happy to walk through any of it.
