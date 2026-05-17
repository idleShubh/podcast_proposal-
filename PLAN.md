# Plan: "Cluely for Founder-Led Sales" — Product Strategy & Starting Point

## Context

You want to build a real-time AI sales assistant — "Cluely for sales" — that listens to a sales call and gives the seller live guidance on how to lead the conversation, which features to bring up, how to interpret the buyer's questions, and what discovery questions to ask. Your motivating question: **is this even worth building, and if so how?**

This plan is the output of fresh web research (May 2026) into the competitive landscape, market size, technical state of the art, adoption realities, and legal/privacy constraints. It then narrows to one specific wedge — **founder-led sales (solo founders and first-AE-at-an-early-stage-startup)** — and lays out an opinionated 90-day path to validate the idea cheaply before committing.

**No code is being written. This is strategy + research + a starting point.**

---

## TL;DR — Honest Verdict

- **The horizontal "Cluely for sales" market is saturated and not worth entering as-is.** ~12 well-funded, shipping competitors already. A YC X25 startup, **Nomi**, is doing literally exactly what you described at $99/mo. Aircover ($3M seed), Attention ($399/user/mo), Sybill, Cirrus Insight, Alpharun, Trellus (YC W22), Revenue.io and Cluely itself have all converged on the same product shape: meeting bot + live transcript + objection prompts + post-call summary.
- **There is, however, a real wedge:** **founder-led sales for solo/early-stage founders** — the cohort doing their own sales before any sales hire. Every existing tool is priced ($99–$399/user/mo) and UX-built for 20+ rep teams with Salesforce and a RevOps function. Founders are systematically excluded.
- **Recommendation: build it, but as a sharp PLG product called "Pitch Copilot for Founders" (working name) at $29/mo, NOT a horizontal Cluely.** Validation budget: $0–$2K and 90 days. Kill the idea if you can't get 25 paying founders by day 90.
- **Defensibility is weak.** This is a thin wrapper over a meeting bot + an LLM. Your only moats are (a) sharp positioning + community + content, (b) playbook data captured from real founder calls, (c) speed of execution. If you don't ship in <6 weeks, Nomi will probably ship a $29 "founder tier" first.
- **Walk away if:** you don't have unfair distribution into the founder community OR you don't already viscerally feel the pain (you've sold to 20+ customers yourself in the last 12 months).

---

## 1. Competitive Landscape (May 2026)

### 1.1 Direct competitors — real-time AI sales copilots

| Product | Approach | Pricing | Funding / Stage | Key signal |
|---|---|---|---|---|
| **Nomi** (nomi.so, YC X25) | Meeting bot, live phrase suggestions, custom playbook | **$99/mo entry** | YC X25, rebranded from HeyNomi | Closest analog to what you described. Claims 12% close-rate lift; one customer "$100K → $360K in 2 weeks" |
| **Aircover** (aircover.ai) | "Virtual sales engineer" on every call, deal-aware pre-brief + live answers | Enterprise, opaque | $3M seed (Defy Partners) | Only **3 G2 reviews** vs Gong's 6,500 — distribution is HARD even with funding |
| **Attention** (attention.com) | Real-time + post-call + AI agents for follow-up | **$399/user/mo enterprise** | Series A | Heavy enterprise positioning, opaque pricing |
| **Sybill** (sybill.ai) | "Behavior AI" — verbal + non-verbal cues, real-time coaching insights | Mid-market | Funded | Differentiates on non-verbal signal reading |
| **Cirrus Insight** | Real-time in-call + Salesforce-native | Enterprise | Established | Salesforce-anchored; not for founders |
| **Alpharun** | "Sentence-level guidance" during live calls, learns from your top performers | Enterprise | Funded | Strongest "best-rep-pattern" angle |
| **Trellus** (YC W22) | Real-time AI for SDR cold calls, embeds in Salesloft/Outreach/HubSpot/Apollo | $50+/mo | YC W22, MIT founders | Owns the SDR cold-call niche |
| **Revenue.io** | Live coaching + pipeline + Salesforce-native | Enterprise | Established | Mature, full RevOps platform |
| **Siro** (siro.ai) | In-person field sales — captures + analyzes in-person convos | Mid-market | Funded | Owns the in-person/field-sales niche — "boost in-person sales 36%" |
| **Aircall / Dialpad / Kixie** | Phone-system-native AI coaching | $40–$95/user/mo | Established | Bundled into the phone platform; only works inside their dialer |
| **Cluely** (cluely.com) | Invisible overlay (DirectX/Metal hooks), originally interview-cheating, now positioned as meeting assistant | $20/mo | **$20.3M raised** (a16z), CEO **admitted fabricating $7M ARR**; real ARR ~$5.2M, 66 employees | Notorious; legal/ethical baggage; pivoting to "legitimate" sales use |

### 1.2 Adjacent — post-call conversation intelligence (not direct competitors but compete for budget)

Gong, Chorus, Fireflies, Avoma, tldv, Fathom, Claap. Gong alone has ~6,500 G2 reviews and is the 800-lb gorilla. They will keep adding real-time features.

### 1.3 Cluely-style stealth overlays (mostly interview-focused; some sales bleed-over)

Cluely, Glass (open source, free), Pluely (open source, 10MB Tauri), OpenCluely, Natively, MindWhisper, Shadow Claude, FinalRoundAI, ParakeetAI, LockedIn AI, HuddleMate.

**Important pattern:** every paid stealth tool has multiple free open-source clones within months. The technical moat is ~zero.

### 1.4 What this tells us
- **The technical capability is commoditized.** Real-time STT (Deepgram Nova-3 / Flux ~450ms), streaming LLMs (Claude Haiku / GPT-4o-mini), meeting-bot SDKs (Recall.ai, Zoom Meeting SDK) — anyone can wire it up in a weekend.
- **The moats that matter:** distribution, positioning, vertical/persona-specific data, brand.
- **Cluely's $20.3M raise + ARR fabrication scandal** is a warning sign: even with a16z money and viral marketing, this category struggles to produce honest revenue. Take the "$120M valuation" stories with massive salt.

---

## 2. Market Reality

- **Conversation intelligence platform market**: $4.54B (2026) → $41.78B (2035) at 28% CAGR. Real category, real budget. *(Business Research Insights)*
- **Adoption is the bottleneck, not demand.** "Most sales coaching platforms fail, with only 15% adoption after three months." Reps don't use the live prompts. The boxed conclusion across the research: **building the prompts is easy; getting reps to actually read/act on them in the moment is the hard problem nobody has solved.**
- **Discovery quality is the empirically validated lever**: Gong's 35K-call study — deals with 11–14 discovery questions close at **74% higher rates**; 3+ discovery questions in cold calls → **2.7x higher meeting conversion**. This is your North Star metric.
- **73% of sales managers spend <5% of time coaching**; managers review only 1–2% of their team's calls. This is the macro pull that funded the whole category.

---

## 3. Your Wedge — "Pitch Copilot for Founders"

You chose: **founder-led sales (solo / early-stage).** Here's why it's defensible enough to try.

### 3.1 Why this wedge is real
1. **Underserved by every competitor.** Nomi at $99/mo, Aircover/Sybill/Attention enterprise-only, Gong $1.2K/user/mo. None of them target the single founder doing 5 calls/week before they hire an AE.
2. **Founder-led sales is the standard early-stage playbook.** YC, a16z, every accelerator preaches "founder sells until $1–2M ARR." That's 2–3 years of acute pain per founder.
3. **They have no playbook, no Salesforce, no RevOps, no manager** — so they're the *exact buyer* for an AI that fills those gaps. They need a "senior sales advisor in a box."
4. **PLG-buyable.** No procurement, no SOC2 check (yet), no committee. Founder swipes a card at $29 if it works once.
5. **The pre-call research problem is acute.** Founders walk into calls cold. Even imperfect auto-brief saves 30 min × 5 calls/week = 2.5 hrs/week. That alone justifies $29/mo.
6. **High-LTV upgrade path.** When the founder hires AE #1, you upsell to a team plan. You ride the customer's growth.

### 3.2 Why this wedge could fail
1. **Founders are cheap and have notoriously short attention spans.** Churn risk is high.
2. **Nomi can launch a "founder tier" at $29 in a weekend.** Your only defense is shipping faster + owning the founder narrative.
3. **Founders are also AI-native and will build it themselves** with Claude + Recall.ai if you charge too much or too little value.
4. **The cohort is small** — maybe 50–100K addressable founders globally doing real sales. TAM caps you somewhere around $20–30M ARR before you have to expand persona.
5. **Distribution is brutal.** Reaching founders requires either (a) you already have a personal brand or (b) you do extreme content/community work for 6–12 months.

### 3.3 Sharp positioning (working draft — to refine in validation)
> **"Pitch Copilot — the AI sales coach for founders selling their own product."**
>
> Auto-researches every prospect 5 minutes before the call. Tells you what to say when they push back. Writes the follow-up while you're still on Zoom. $29/mo. No sales team required.

Sub-promises:
- "You'll never walk into a call cold again."
- "Get the discovery questions your investors would ask."
- "Sound like a senior founder, even on call #2."

---

## 4. The Product (MVP scope)

The MVP is a meeting-bot SaaS, not a stealth overlay. Reasons:
- Founders selling their own product **don't need to hide the assistant from themselves** — Cluely's overlay tech is a solution to the interview-cheating use case, not founder sales.
- Meeting bots are 5x cheaper and 10x faster to build (no native macOS/Windows GPU work).
- Bots have legal/consent precedent and infra (Recall.ai, Vexa, etc.).
- You can layer a stealth overlay later as a "premium" mode if customers ask.

### 4.1 Core MVP features (6-week scope)

**A. Pre-call brief (the wedge — most important)**
- Input: calendar invite or one-click "brief this call" from Cal.com / Google Calendar
- Output (delivered 5 min before call, also re-accessible during): one-page brief with
  - Prospect: name, role, tenure, LinkedIn highlights, recent posts/podcasts
  - Company: 1-line description, headcount, recent funding, last 2 product launches, 3 most-recent press mentions, hiring signals
  - Conversation hooks: 3 specific "openers" tied to recent activity
  - Likely objections (LLM-inferred from company stage + industry + your product category)
  - Suggested discovery questions tailored to their stage (MEDDIC + SPIN-flavored)

**B. Live in-call assistant (minimal, surgical)**
- Joins as a meeting bot in Zoom (Meet/Teams in v2)
- Streaming transcript visible on a side panel (web app open on second screen)
- **Max 1 prompt card visible at a time** — research shows reps ignore walls of text
- 3 prompt types only:
  1. **Discovery nudge** — "You've talked for 3 min. Ask a discovery question. Suggest: '…'"
  2. **Objection responder** — auto-detects objection ("too expensive", "no budget", "need to think") and shows a one-line response template
  3. **Missed-feature reminder** — based on the prospect's stated need, flags features you haven't mentioned that are likely to land
- A talk:listen ratio meter (industry truth: top performers talk 40%, listen 60%)
- Hotkey to mark "this moment is gold" — used post-call to extract clips

**C. Post-call deliverable (instant value)**
- 60-second structured summary: pain points, asks, objections raised, next step committed
- Draft follow-up email pre-written in *your voice* (uses your prior emails as style anchor — 2-shot)
- One-click export to Notion / clipboard / Gmail draft
- Optional CRM sync to **HubSpot Free / Attio / Folk** (NOT Salesforce — wrong persona)

**D. The "Playbook Engine" (the moat over time)**
- Captures every closed-won and closed-lost conversation
- Asks the founder a 30-sec post-mortem ("Why did this close? Why didn't it?")
- After ~10 calls, starts personalizing the prompt-cards from your own win patterns
- This is the data flywheel: more calls → better hints → less churn → harder for Nomi to copy

### 4.2 NOT in scope for MVP (defer to v2/v3)
- Stealth overlay mode (only build if 25%+ of beta users request it)
- Microsoft Teams / Google Meet (start Zoom-only; Recall.ai abstracts this anyway)
- Multi-language (English-only)
- Mobile app (web app is enough; Zoom calls happen on laptops)
- Team features (you're not selling to teams yet)
- Salesforce integration (wrong persona)
- LinkedIn integration that scrapes (legal hot stove)
- Auto-dialer / outbound (Trellus owns SDR cold-call; don't fight them)
- Real-time voice analysis (sentiment, tone) — interesting but Sybill owns it

### 4.3 The single product decision that matters most
**Do NOT show a real-time transcript with floating tips like every competitor does.** That UI doesn't get used during the call because the founder is *talking and listening*. Instead:

- **Pre-call brief is the always-open tab.** Founder glances at it.
- **In-call: just one card.** When something material happens (objection, missed feature, talk-time imbalance), surface ONE actionable line. Otherwise stay invisible.
- **Post-call summary + email is the daily wow.**

This is the design counter-positioning vs Nomi/Aircover (who pile on tips and lose). If reps only use 15% of these tools, build the 15% that gets used.

---

## 5. Technical Architecture

### 5.1 Stack (opinionated, picked for speed-to-MVP)

| Layer | Pick | Reason | Approx cost |
|---|---|---|---|
| Meeting bot infra | **Recall.ai** | Don't build your own bot. Recall handles Zoom/Meet/Teams + waiting room + recording compliance. | ~$0.02/min |
| Speech-to-text | **Deepgram Nova-3 streaming** (or Flux for voice-agent mode) | ~450ms latency, $0.0036/min, 6.84% WER | ~$0.22/hr |
| LLM — fast hints | **Claude Haiku 4.5** or **GPT-4o-mini** | Cheap + fast for short prompt cards | ~$0.05–0.15/call |
| LLM — pre-call brief + post-call summary | **Claude Sonnet 4.6** | Reasoning quality matters more than latency here | ~$0.10–0.30/call |
| Web research for pre-call brief | **Perplexity API** or **Exa.ai** + LinkedIn-allowed sources (Crunchbase, news, founder's own posts) | Don't scrape LinkedIn directly | ~$0.05/brief |
| Frontend | **Next.js + Tailwind + shadcn/ui** on Vercel | Fast, well-known, free tier covers MVP | $0 to start |
| Auth + DB | **Supabase** | Postgres + auth + realtime + storage in one | $0 to start |
| Background jobs | **Inngest** or **Trigger.dev** | For pre-call brief generation, post-call summary | Free tier |
| CRM connectors | **Paragon** or hand-roll for HubSpot + Attio | Avoid building all connectors yourself | $0 to start |
| Email | **Resend** for transactional, **Loops** for marketing | | $0 to start |
| Analytics | **PostHog** | Funnels + session replay + flags in one | Free tier |
| Calendar integration | **Cal.com webhook** + **Google Calendar API** | Trigger pre-call brief generation | $0 |
| Voice style cloning (email tone) | **OpenAI gpt-4o** few-shot on stored sent emails | Don't fine-tune | included above |

### 5.2 Unit economics (back-of-envelope, must validate)

Assumption: typical user has 5 calls/week × 30 min = 2.5 hrs/week of audio.

| Cost | Per call (30 min) | Per user / month (20 calls) |
|---|---|---|
| Recall.ai meeting bot | $0.60 | $12.00 |
| Deepgram STT | $0.11 | $2.20 |
| LLM hints (Haiku, ~30 turns) | $0.10 | $2.00 |
| Pre-call brief (Sonnet + Exa) | $0.30 | $6.00 |
| Post-call summary + email (Sonnet) | $0.15 | $3.00 |
| Infra (Supabase, Vercel, etc.) | — | $1.00 |
| **Total COGS / user / month** | **~$1.26 / call** | **~$26.20** |

At **$29/mo retail**, this is roughly break-even on heavy users. Implications:
- **You must aggressively cache** (re-use the same prospect brief across multiple reps, reuse company research).
- **Tiering** likely needed: $29/mo for 20 calls/mo, $79/mo unlimited. Or move bot infra to a per-call passthrough.
- **You probably can't sustainably sell at $29/mo until you hit ~1000 users and can negotiate Recall + Deepgram volume discounts.** Plan for $39–49/mo as the "true" price; use $29 as a launch promo for the first 200.
- **Free tier is dangerous** — Recall costs are real. Cap free at 2 calls total (not /month).

### 5.3 Latency budget
End-to-end target for in-call hints: <2 seconds from end-of-prospect-utterance to card appearing.
- STT streaming + endpointing: ~500–800 ms
- LLM hint generation (Haiku, 100 tokens out): ~400–800 ms
- Network + rendering: ~200 ms
- Buffer: ~200 ms

Achievable. Don't try sub-second; not needed for sales (it's needed for interview-cheating, which is Cluely's actual moat).

### 5.4 What to do, what to NOT build
- **Don't build the meeting bot, the STT engine, the CRM connectors, the auth system, or your own LLM.** Buy/rent all of these.
- **Do build:** the prompt-engineering layer (this is your IP), the playbook engine (your data moat), the pre-call brief composer (your wedge), and the founder-centric UX (your differentiator).
- This means MVP is **~3000 LOC, 4–6 weeks for a solo builder using Claude Code**, $50–200/mo infra during validation.

---

## 6. Go-to-Market — the part most founders underestimate

**Reality check:** Aircover raised $3M and has **3 G2 reviews**. Cluely has $20M and faked its revenue. Distribution is the actual hard part, not the tech.

### 6.1 Channels, ranked by leverage for the founder-led wedge

1. **Build-in-public on X / LinkedIn.** Daily teardowns of bad pitch behavior, before/after call clips (anonymized), screenshots of the pre-call brief generating from a famous startup's deck. This is your single highest-leverage activity. Plan to spend 30% of your time here for the first 6 months.
2. **YC Bookface / YC alumni Slack.** Free for YC founders → land 20 design partners. Their endorsement is worth more than $50K of ads.
3. **Indie Hackers / Hacker News launch.** The HN crowd is your buyer; Show HN with a free tier converts well for dev-flavored sales tools.
4. **Product Hunt launch.** Coordinated, plan for 4 weeks out. Expect 200–500 signups, 5–20 paying within 30 days.
5. **Targeted founder content collabs.** Lenny Rachitsky, Pete Sena, Wes Bos, Theo, Pieter Levels — get one big founder voice to use it on a livestream.
6. **Cohort partnerships.** YC, Antler, On Deck, Pioneer, OpenAI Startup Fund — "free for your batch."
7. **NOT this list, do NOT bother:** Google Ads (CAC too high for $29 ACV), outbound SDR (you ARE the SDR being replaced), conference booths (wrong audience), generic SaaS review sites.

### 6.2 First 100 customers playbook
- 0–10: hand-deliver. You sit in on their first 3 calls (concierge mode). Get a video testimonial.
- 10–50: Show HN + Product Hunt + 1 build-in-public launch tweet per week.
- 50–100: 1 paid integration (Cal.com or HubSpot Free Marketplace listing) + 3 founder-podcast guest spots.

### 6.3 Pricing strategy
- **Beta (months 1–3):** Free for design partners (≤20 founders). Get the data flywheel started.
- **Launch (month 4):** $29/mo "Founder" tier, 20 calls/mo. Annual at $290 (2 months free).
- **Month 6–9:** Add **$79/mo "Founder+" tier** with unlimited calls + Folk/Attio sync.
- **Month 12+:** Add **$249/mo "Small Team" tier** (3 seats) once a founder makes their first AE hire. This is the LTV move.

---

## 7. Risks & What Could Kill It

| Risk | Likelihood | Severity | Mitigation |
|---|---|---|---|
| Nomi launches a $29 founder tier | High | High | Ship in <6 weeks. Out-position with founder-native UX (HubSpot Free, Attio, Cal.com, Notion — not Salesforce). Build community moat. |
| Cluely pivots into sales aggressively | Medium | High | Lean into "honest, no-stealth, founder-built" positioning. Cluely's brand is damaged (CEO admitted fraud). |
| Recall.ai / Deepgram raise prices | Medium | Medium | Negotiate annual deals at 500+ users. Have a fallback (Vexa for self-hosted Whisper). |
| Zoom builds it natively | Medium | High | Zoom AI Companion already exists. Your defense: founders don't use Zoom AI for their own sales — it's an admin/IT product. You're a vertical UX play. |
| Legal/consent issues (EU all-party consent, H&M €35M precedent) | Medium | High | Bot ALWAYS announces itself, transcript ALWAYS visible to all parties. Never go stealth. Default region settings respect 2-party consent jurisdictions. SOC2 by month 9 (use Vanta/Drata). |
| Founders churn after 30 days ("I learned how to sell, don't need it") | High | High | Make the pre-call brief the irreplaceable feature, not the in-call hints. The brief is utility that compounds with usage. |
| LLM costs eat margin | Medium | Medium | Aggressive caching, prompt distillation, batch the post-call work. Move heavy users to higher tier. |
| You can't reach founders | Medium | Critical | Validate by month 1 — if you can't get 10 founder interviews in 30 days, the distribution problem will kill the product later. |
| LinkedIn / X / Crunchbase shut off your data sources | Medium | Medium | Build on official APIs only (LinkedIn Sales Navigator API, Crunchbase API, Exa). Avoid scraping. |

### 7.1 Legal must-dos
- **Consent disclosure:** bot announces itself on join. Founder gets a notice template to send to prospects in calendar invite.
- **2-party consent regions:** explicitly require recording opt-in for prospects in CA, FL, IL, MD, MA, MT, NH, PA, WA + entire EU. Default to OFF in these regions until prospect confirms.
- **GDPR/CCPA:** data deletion endpoint, DPA template, EU data residency optional (use Supabase EU region).
- **Don't train on customer call data without explicit opt-in.** Your moat is your prompt engineering + playbook, not raw call data.
- **No stealth mode.** Cluely's overlay approach is technically legal but reputationally toxic for B2B. Do not build it.

---

## 8. 90-Day Validation Plan (cheap, kill-or-build gates)

The goal of the first 90 days is **not to build a polished product** — it's to find out if 25 real founders will pay you for this. Spend <$2K and <100 hrs/week of your time.

### Week 1–2: Demand validation (no code)
- [ ] Interview 15 solo founders / first-AE founders about their sales process
- [ ] Specifically ask: "What do you do in the 10 minutes before a call?" and "When was the last time a call went badly? Why?"
- [ ] Show a Figma mockup of the pre-call brief — gauge "would you pay $29/mo for this?" reaction
- [ ] **Gate:** at least 8/15 say "yes, please ship that" → continue. Else, kill.

### Week 3–4: Concierge MVP (manual, you in the loop)
- [ ] Pick 5 friendly founders. You manually generate their pre-call brief in 30 min before each call
- [ ] You sit in on the call silently and Slack them mid-call with 1–2 hints
- [ ] You write the follow-up email post-call
- [ ] **Gate:** at least 3/5 say "when can I have this as a product?" → continue. Else, the value isn't there.

### Week 5–10: MVP build
- [ ] Stack from §5.1
- [ ] Ship only the 6-week MVP scope from §4.1 — resist scope creep
- [ ] Beta to the 5 concierge users + 15 more from interviews

### Week 11–13: Public launch + monetize
- [ ] Show HN
- [ ] Product Hunt
- [ ] Start charging $29/mo. First 100 customers get the "Founder" badge (status moat)
- [ ] **Day-90 gate:** 25 paying customers OR clear path to 25 within 30 days → continue. Else, kill or pivot.

### Day-90 kill criteria (be honest)
- <10 paying customers despite 1000+ visitors → product not compelling enough
- <30% week-2 retention → in-call hints unused, founders churn
- CAC > $200 with no clear improvement path → distribution unsolvable for $29 ACV
- Nomi or Cluely launches an indistinguishable $29 founder tier before you ship → you lost the race

---

## 9. Decision Framework — Should YOU build this?

Score yourself 0–2 on each. Build only if you score 8+/12.

| Question | Score (0/1/2) |
|---|---|
| Have you personally sold to 20+ customers in the last 12 months? | |
| Do you have a public/founder audience of 5K+? | |
| Can you ship a 6-week MVP solo (or with one cofounder)? | |
| Do you have $20K+ of runway to invest with no revenue for 6 months? | |
| Do you have direct intros into 30+ early-stage founders? | |
| Are you willing to do public content (X, podcasts) 3x/week for a year? | |

- **8–12:** Build. The wedge is real and you have unfair advantages.
- **5–7:** Build only after fixing the gap (e.g., spend 3 months building audience before building product).
- **<5:** Don't build this. The thin technical moat means execution + distribution carry 100% of the load. You'll be out-shipped by Nomi.

---

## 10. What I'd do if this were my project (opinionated)

1. **This week:** Open a Notion doc. List every solo founder you know personally who's actively selling. Cold email 15. Get 8 on a call.
2. **Don't write a line of code until after week 2.** Validate the pre-call brief is the wedge, not the in-call hints. (My strong prior: the brief is the irreplaceable feature.)
3. **Park the name "Cluely for sales."** That framing positions you as a follower. Pick a name that signals "for founders": *Pitch Copilot, Founder Sells, Cold→Close, Pretrade.* Run a quick survey.
4. **Pre-announce on X with the Figma mock** before building. Get a waitlist of 200+ before shipping. This both validates demand and seeds launch-day distribution.
5. **Make the pre-call brief generate-able for free for the first 1 prospect** (no signup) — pure top-of-funnel hook. The "wow" is the brief, not the in-call hints.
6. **Skip the meeting bot entirely for V0.** Just ship the pre-call brief as a Chrome extension on Google Calendar. Charge $9/mo. Add the bot in V1 once you've proven the brief is the wedge.

That last point is the contrarian one. If I'm right, the brief alone is a real product. The meeting-bot layer just gets you into Nomi's war. Test the cheaper, narrower V0 first.

---

## 11. Verification — How to Test the Plan Before Committing

This plan is a hypothesis, not a fact. Validate it cheaply:

1. **Talk to 15 founders this week.** If <8 of them describe the pre-call prep pain in their own words (without prompting), the wedge isn't real. Kill.
2. **Sign up for Nomi, Aircover, Sybill, Cluely.** Use them for a week each. Take notes on what they get wrong for founders specifically. If you find they nail the founder use case, the wedge is closed. Kill or re-pick from §3.
3. **Post the working name + 1-line positioning on X.** If you get <50 likes and 0 DMs from real founders, your distribution assumption is wrong. Either build audience first or kill.
4. **Cost-model with real Recall.ai/Deepgram quotes.** Email both vendors for startup pricing. If COGS comes in >$1.50/call at MVP scale, the $29/mo tier is unviable — re-price or re-design.

If all four checks pass, build the V0 brief-only product in 2 weeks.

---

## 12. Critical Files / Artifacts (none yet — this is a greenfield plan)

There is no codebase yet. Future plan files to create as you proceed:
- `~/.claude/plans/founder-pitch-mvp-spec.md` — once you commit to the build, the spec for the 6-week MVP
- `~/.claude/plans/founder-interviews-notes.md` — notes from the 15 founder interviews
- `~/.claude/plans/pitch-copilot-pricing-model.md` — full COGS spreadsheet once you have vendor quotes

---

## Sources (May 2026 research)

- Cluely: [TechCrunch — Cluely ARR doubled to $7M](https://techcrunch.com/2025/07/03/cluelys-arr-doubled-in-a-week-to-7m-founder-roy-lee-says-but-rivals-are-coming/), [TechBuzz — CEO admits fabricating revenue](https://www.techbuzz.ai/articles/cluely-ceo-admits-fabricating-7m-revenue-in-rare-fraud-confession), [Wikipedia — Cluely](https://en.wikipedia.org/wiki/Cluely), [Tracxn profile](https://tracxn.com/d/companies/cluely/__Ju-PhvKyO8Kv2MD9Esgxhmh_EB15mxqSDhhJ2zxBqN0)
- Nomi: [Nomi homepage](https://www.nomi.so/), [Nomi pricing](https://www.nomi.so/pricing), [YC profile](https://www.ycombinator.com/companies/nomi)
- Aircover: [Aircover homepage](https://www.aircover.ai/), [Crunchbase](https://www.crunchbase.com/organization/aircover), [Ridge Ventures seed announcement](https://medium.com/ridgevc/smooth-sale-ing-aircovers-seed-round-a-watershed-moment-for-in-meeting-sales-tools-a2e7d9d7668a)
- Attention: [Attention homepage](https://www.attention.com/), [G2 reviews](https://www.g2.com/products/attention/reviews), [Dimmo pricing review](https://www.dimmo.ai/products/attention)
- Sybill: [Sybill homepage](https://www.sybill.ai/), [Coaching/performance](https://www.sybill.ai/coaching-performance)
- Trellus: [Trellus homepage](https://www.trellus.ai/), [YC launch](https://www.ycombinator.com/launches/Htw-trellus-real-time-sales-ai-coach-for-cold-calls)
- Siro (in-person sales): [Siro homepage](https://www.siro.ai/)
- Gong vs Chorus + real-time alternatives: [Cirrus Insight comparison](https://www.cirrusinsight.com/gong-vs-chorus), [Revenue.io alternatives list](https://www.revenue.io/blog/best-gong-alternatives-and-competitors), [Balto alternatives](https://www.balto.ai/competitors/gong-alternatives/)
- Real-time AI sales assistants overview: [Prospeo](https://prospeo.io/s/real-time-ai-sales-assistant), [Cirrus Insight AI sales coaching guide](https://www.cirrusinsight.com/blog/ai-sales-coaching), [Trellus best real-time tools list](https://www.trellus.ai/post/best-real-time-ai-sales-call-assistant)
- Discovery / methodologies: [Sybill on discovery questions](https://www.sybill.ai/blogs/best-discovery-questions), [Avoma discovery playbook](https://www.avoma.com/blog/discovery-call), [Oliv on MEDDIC + AI](https://www.oliv.ai/blog/meddic-sales-methodology), [Eagr B2B methodologies comparison](https://eagr.ai/blog/b2b-sales-methodologies-compared)
- Adoption / coaching reality: [MySalesCoach — 6 deadly sins of coaching](https://www.mysalescoach.com/blog/sales-coaching-mistakes), [Hyperbound — sales coaching platforms reviewed](https://www.hyperbound.ai/blog/sales-coaching-platforms-review), [Reply — what works in AI sales coaching](https://reply.io/blog/ai-sales-coaching/)
- Tech / latency: [Deepgram low-latency voice AI](https://deepgram.com/learn/low-latency-voice-ai), [Whisper vs Deepgram 2025](https://deepgram.com/learn/whisper-vs-deepgram), [NextLevel best STT models 2026](https://nextlevel.ai/best-speech-to-text-models/), [CodeSOTA speech recognition 2026](https://www.codesota.com/guides/speech-recognition)
- Privacy / legal: [tldv on bot-free recording legality](https://tldv.io/blog/is-bot-free-recording-legal/), [Sally.io on Zoom AI + GDPR](https://www.sally.io/blog/zoom-ai-companion-gdpr-and-data-protection), [Cornell IT — blocking AI bots from Zoom](https://it.cornell.edu/zoom/zoom-block-ai-bots)
- Market sizing: [Business Research Insights — Conversation Intelligence Platform Market](https://www.businessresearchinsights.com/market-reports/conversation-intelligence-platform-market-102311), [GII Research — Conversation Intelligence Software 2026](https://www.giiresearch.com/report/tbrc1963302-conversation-intelligence-software-global-market.html)
- Vertical SaaS context: [Mayfield — AI transforming vertical SaaS](https://www.mayfield.com/how-ai-is-transforming-vertical-saas/), [SignalFire — frameworks for AI vertical SaaS](https://www.signalfire.com/blog/frameworks-for-ai-vertical-saas), [a16z — "AI Inside" opens new vSaaS markets](https://a16z.com/vsaas-vertical-saas-ai-opens-new-markets/), [Bessemer — building vertical AI](https://www.bvp.com/atlas/building-vertical-ai-an-early-stage-playbook-for-founders)
- Cluely overlay alternatives (signal of commoditization): [GitHub — Pluely](https://github.com/iamsrikanthnani/pluely), [GitHub — OpenCluely](https://github.com/TechyCSR/OpenCluely), [Hyperlush — Cluely vs Glass open source](https://hyperlush.com/cluely-vs-glass/)
