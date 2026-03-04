---
title: "TasteGraph"
tagline: "Stake your taste. Discover what you'll love."
author: "Jeremie"
date: "2026-03-04"
status: "draft"
tags:
  - recipes
  - food
  - social
  - personalization
  - taste-profile
  - staking
intuition_atoms: []
github_discussion: ""
---

# TasteGraph

> Stake your taste. Discover what you'll love.

## Problem

Recipe apps today are siloed — your saved recipes, ratings, and preferences are trapped inside each platform. If you switch from one app to another, you start from scratch. Worse, these apps barely know what you actually like. They recommend based on what's popular, not what fits *your* palate. And when you're cooking for friends, there's no easy way to find a recipe that works for everyone's tastes, dietary needs, and preferences.

People scroll through endless recipe feeds hoping to find something good. They text friends "any allergies?" before dinner parties. They mentally track what ingredients they love or hate. Some keep notes in spreadsheets or bookmarks scattered across apps. None of it is connected, portable, or smart.

## Solution

TasteGraph lets you build a portable taste profile by staking on ingredients and recipes. Stake *for* things you love, stake *against* things you hate — the amount reflects how strongly you feel. This profile lives on the Intuition knowledge graph, so any app can read it. Then TasteGraph uses everyone's profiles to recommend recipes you'll actually enjoy — and when you're hosting friends, it cross-references everyone's preferences to suggest the perfect dinner menu.

### User Journey

1. **Set up your taste profile** — Browse ingredients, stake for your favorites (big stake on garlic, small stake on basil), stake against the ones you can't stand. You now have an on-chain food identity.
2. **Discover recipes** — TasteGraph recommends recipes weighted by your staked preferences. High-conviction ingredients get prioritized, dealbreakers get filtered out.
3. **Plan social meals** — Invite friends to a dinner event. The app reads everyone's taste profiles and suggests recipes that maximize group happiness — avoiding hard "no"s and leaning into shared loves.
4. **Share & curate** — Post your own recipes. Others can stake on them to signal quality. The best recipes rise based on real conviction, not just likes.

## How It Uses Intuition

| Protocol Feature | How It's Used |
|-----------------|---------------|
| Atoms | Each ingredient (garlic, cilantro, anchovy...), each recipe, and each user profile becomes an atom — a permanent entry in the knowledge graph. |
| Triples | Relationships like `[User] → loves → [Garlic]`, `[Recipe] → contains → [Basil]`, `[User] → recommends → [Recipe]`. These connect everything together. |
| Staking/Vaults | Users stake FOR ingredients they love and AGAINST ones they hate. The amount = conviction strength. Staking on recipes signals quality. This creates a rich, nuanced preference system — not just binary like/dislike. |
| Knowledge Graph | The app reads the graph to power recommendations. Cross-referencing multiple users' staked preferences enables the social dinner planning feature. Any other app can also read these preferences — your taste profile is portable. |

### Why This Needs Intuition

Without Intuition, this is just another recipe app with a rating system. The protocol gives you three things no centralized app can:

1. **Portability** — Your taste profile isn't locked in one app. It's on-chain, readable by any app that connects to the knowledge graph.
2. **Nuanced signal** — Staking with real tokens creates a spectrum of preference strength that simple likes/stars can't match. There's a cost to signaling, so the data is more honest.
3. **Composability** — The social dinner feature only works because everyone's preferences live in the same open graph. No API partnerships needed — it's all public data.

## Target Users

**Primary audience:** Food-curious people who already use recipe apps (AllRecipes, Paprika, Mela, etc.) and are frustrated by generic recommendations. They care about what they eat, cook regularly, and often host friends or family for meals. Bonus: they're open to web3 or already in the Intuition ecosystem.

**First 100 users would be:**

- **Intuition community members** who cook — they already understand staking and atoms, so onboarding is easy. Reach them through Discord/Telegram.
- **Home cooks who host** — people who regularly have friends over for dinner and deal with the "what should I make?" problem. Food subreddits, cooking communities, foodie Discord servers.
- **People with dietary restrictions** — vegans, people with allergies, picky eaters. They'd instantly see the value of a system that *remembers* and *communicates* their preferences across apps and social contexts.

## Business Model

- **Protocol staking rewards** — Every time users stake on ingredients or recipes, the protocol's economic mechanics kick in. TasteGraph could take a small fee on staking activity within the app.
- **Premium features** — Free to build your taste profile and browse recipes. Pay for advanced features like: dinner party planning for large groups, AI-powered meal planning for the week, grocery list generation based on chosen recipes.
- **Recipe creator monetization** — Popular recipe creators could earn a share of the stakes placed on their recipes. This incentivizes high-quality content and gives TasteGraph a cut as the platform.
- **Ecosystem grants** — Early funding through Intuition ecosystem grants to bootstrap development and user acquisition.
- **Brand partnerships** — Down the road, food brands could sponsor ingredient atoms or get visibility in recommendations (clearly labeled). They'd pay for access to honest, staked preference data — far richer than traditional surveys.

## Strengths & Risks

**Strengths:**

- Staking FOR/AGAINST is a genuinely novel preference system — way richer than likes or stars
- The social dinner planning feature is a strong differentiator no existing app offers
- Deep Intuition fit — staking isn't bolted on, it IS the core product
- Portability is a compelling long-term story (your taste profile works everywhere)
- Solves the "fake reviews" problem — staking real tokens makes preferences honest

**Risks to address:**

- **Cold start** — Needs seeded recipe data and a fast, fun onboarding to be useful from day one → Mitigation: Seed with open-source recipe datasets, swipe-style ingredient quiz for instant profile setup
- **Crypto UX barrier** — Must abstract away web3 complexity or risk losing mainstream users → Mitigation: Email signup, hide wallet/token language behind food-friendly UI ("How much do you love garlic?" instead of "Stake on garlic")
- **Recommendation engine** — Group preference aggregation requires custom off-chain logic on top of the protocol → Mitigation: Start with simple weighted matching, iterate with user feedback
- **Network effect dependency** — Dinner party feature gets better with more friends on the platform → Mitigation: Launch personal taste profile + recipe discovery first (MVP), add social features in v2

## Next Steps

1. Build a taste profile MVP — ingredient staking UI with swipe-style onboarding, connected to Intuition atoms/vaults
2. Seed the recipe graph — import an open-source recipe dataset as atoms with ingredient triples
3. Build the recommendation engine — match recipes to a user's staked preferences, weighted by conviction

---

*Submitted via the [Intuition Ideation Skill](https://github.com/0xIntuition/agent-skills)*
