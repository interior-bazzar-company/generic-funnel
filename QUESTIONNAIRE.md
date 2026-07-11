# Sales funnel questionnaire — proposed

Audience: interior business owners in India, arriving cold from a Meta or Google ad.
Goal of the form: qualify them (can they pay, do they need us, how urgent), and get a phone number.

## The rules this follows

1. **Easy first, hard last.** Early questions cost nothing to answer and are about *them*. Money and contact details come after they've invested effort.
2. **One question per screen**, big tappable options, no typing until the last step.
3. **Their words, not ours.** "How do you get clients today?" — not "What is your current lead acquisition channel?"
4. **Every question earns its place.** It must either score the lead, route the sale, or make the next question easier. If it only feeds a report, cut it.
5. **7 steps maximum.** Each extra step costs completions.

## The questions, in order

### Step 1 — What kind of work do you do?
*Multi-select. Select all that apply.*

Easiest possible opener: it's their identity, there's no wrong answer, and picking a chip is a micro-commitment that pulls them into the form.

- Residential homes
- Offices / workspaces
- Shops / showrooms
- Hotels & restaurants
- Hospitals / clinics
- Schools / colleges
- Factories / warehouses
- We do everything

### Step 2 — Which city do you work in?
*Multi-select + "Other city" free text.*

Still easy, and it's the question that makes the exclusivity promise real — "one spot per area" only means something once they've named their area.

Delhi NCR · Mumbai · Bengaluru · Pune · Hyderabad · Chennai · Kolkata · Ahmedabad · Other city

### Step 3 — How do you get most of your clients today?
*Single-select.* **(new — replaces nothing, this is the missing question)*

This is the most valuable question on the form and it currently isn't asked. It tells the sales team exactly which pitch to open with, and it tells you which competitor you're displacing.

- Justdial, IndiaMART or similar
- Facebook / Instagram ads
- Google ads
- An agency runs it for me
- Word of mouth and referrals
- Walk-ins and my own contacts

### Step 4 — What annoys you most about the leads you get?
*Single-select.*

They've now told you where leads come from; this asks why it hurts. The answer is the exact sentence the salesperson repeats back on the call.

- The same lead goes to my competitors too
- Most of them are not serious
- They don't pick up the phone
- Everyone only asks for the lowest price
- I'm just not getting enough leads
- It costs too much for what I get

### Step 5 — How many new projects can you take on next month?
*Single-select.* **(new)*

The honest way to ask "how big are you" without asking for money. It sizes the account, and it's the strongest signal of whether they can actually service exclusive leads.

- 1–2 projects
- 3–5 projects
- 6–10 projects
- More than 10
- Not sure yet

### Step 6 — How much do you spend every month to get new clients?
*Single-select.* **(moved later — currently step 3)*

The single riskiest question on the form. Right now it's asked third, before the visitor has invested anything, and it is almost certainly the biggest drop-off point. Moving it to step 6 means they answer it after five micro-commitments, when quitting feels wasteful.

- Nothing yet — clients come from referrals
- Under ₹50,000 a month
- ₹50,000 – ₹1 lakh
- ₹1 – ₹2 lakh
- ₹2 – ₹2.5 lakh
- More than ₹2.5 lakh

### Step 7 — Where should we send them?
*Contact. The only step with typing.*

- Business name — required
- Your name — required
- Mobile number (+91) — required
- Your role — optional (Owner / Director / Sales head / Manager)
- **Best time to call you** — defaults to "Anytime" (Morning 9–12 · Afternoon 12–4 · Evening 4–8). Nothing raises connect rate more cheaply than calling when they said to call, and a pre-filled default means it costs the visitor zero effort to skip.
- **Where did you hear about us?** — optional (Facebook / Instagram · Google search · A friend told me · WhatsApp · YouTube · Newspaper or news article · Somewhere else)
- Consent checkbox — required

**Cut from this step:** "Website or Instagram" — ask it on the call, or on the thank-you screen. It's the one optional field that buys nothing the salesperson can't get in ten seconds by asking.

## What "driving this right now" becomes

The current step 5 ("What's driving this right now?") overlaps heavily with the frustration question — people who say "leads shared with competitors" also say "losing leads to competitors". It's asking the same thing twice, which is a step you're paying for and not learning from. **Drop it**, and recover urgency from step 5 (capacity) instead, which is harder to fake.

## Scoring and tags

Two labels ride along with each lead.

**`lead_tier`** — who the team calls first. Hot ≥ 70 · Warm 40–69 · Nurture < 40.

| Signal | Points |
|---|---|
| Spend > ₹2.5L | +40 |
| Spend ₹2–2.5L | +30 |
| Spend ₹1–2L | +25 |
| Spend ₹50k–1L | +12 |
| Spend under ₹50k | +5 |
| Spend nothing yet | −5 |
| Can take 6+ projects next month | +20 |
| Can take 3–5 projects | +12 |
| Currently on Justdial / IndiaMART / an agency | +15 (we displace a bill they already pay) |
| Frustration = shared with competitors, or not serious | +20 |
| Role = Owner / Founder | +10 |
| "Not sure yet" on capacity | −10 |

**`plan_fit`** — which plan the salesperson opens with, so they never pitch premium to a referral-only one-man shop.

- **Premium** — spend ≥ ₹1 lakh, *or* capacity ≥ 6 projects
- **Base** — everyone else

Both get sent in the enquiry email subject, so the inbox sorts itself:
`[Hot · 85 · Premium] New enquiry — Perfekte Küchen · ₹2–2.5L`

## Net effect

Same 7 screens as today (6 + contact), but: budget moved from step 3 to step 6, the duplicate urgency question dropped, two better questions added (current lead source, capacity), the "Website or Instagram" field removed from the contact step, and every option rewritten in plain language. "Where did you hear about us?" stays — it's the only attribution you get from people who arrive by referral or word of mouth, which the URL can never tell you.
