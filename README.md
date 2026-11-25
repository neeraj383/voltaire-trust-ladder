# Earned Trust: the Trust Ladder

**Team Voltaire** · Neeraj Preenand, Achintya Iyer, Viyaan Prakash
*Follow the Money: Innovation Challenge, IIM Bangalore CSITM × PayU, 2026. Problem: "The Bakery That Takes Bets".*

A merchant opens a payment account with genuine documents, calls itself a bakery, and quietly collects money for illegal betting. This prototype shows how a payment provider can notice and respond, without punishing honest shops whose sales change for good reasons.

**Live demo:** https://neeraj383.github.io/voltaire-trust-ladder/
Or open `index.html` in any browser (no install, works offline). A guided tour starts on first visit; press **? Guided tour** to replay it.

## The idea in one line
Don't police merchants into proving they're innocent. **Make being real worth proving.**

- **Trust Ladder:** every shop starts on **Level 1 (Starter)**, with payouts sized to similar shops nearby. Real shops climb to Proven, Verified and Trusted by showing proof they already have, and unlock faster payouts, a badge and a loan offer. Fakes can't climb.
- **Three questions** (data PayU already has):
  - **Shape:** does the money look like similar shops?
  - **Control:** is the real owner running it?
  - **Network:** does it share customers with shops it shouldn't?
- **Missing proof never counts as suspicion.** Proof only helps a shop climb.
- **Graduated response:** 1 yes → **ASK**, 2 → **SLOW** (only the unexplained extra waits), 3 → **STOP** (human review, report to FIU-IND). A question left unanswered counts as a yes and keeps counting.
- **Immune-system learning:** "normal" is relearned every week. Every confirmed front is remembered (device, gamblers). A confirmed case of a new trick can add a brand-new check.

## Story mode

A full-screen, self-playing presentation (about 2.5 minutes, 19 scenes) told from PayU's side: PayU's problem and problem statement, how betting rings operate (panels, rented accounts, layering, scale, why rules fail, with sourced facts from ED filings and reporting), the critical-thinking approach (claim, premises, principle; five whys), and our system. Space pauses, arrow keys move, Esc closes.

## Explain like I'm 5

The **Explain like I'm 5** button (top right, and offered on first visit) opens a 13-step illustrated explainer in two chapters:

1. **How we figured it out:** the bakery that takes bets, why one-time KYC misses it, the root cause, why trust has to be earned, protecting honest shops, and why the system must learn.
2. **How it works:** Level 1 for everyone, climbing the ladder, the three questions, counting the yeses, caught and remembered, learning a new check, and the results.

Most steps have a **See it in the demo** button that jumps to the exact week and shop, with a button to come back to the explainer.

## The four views

| Tab | What it shows |
|---|---|
| PayU monitoring | Every shop, every week: trust level, the three questions, money paid or held, the action, why, and who shares customers |
| Merchant app | Three phone modes: shops in the simulation; **Try the sign-up** (OTP, email, Aadhaar e-KYC, PAN, selfie, bank check, GST/Udyam, 3-year sales, suppliers, interstate orders, consent, then matching to the database); and **First weeks and rewards** (level-ups, badge, loan offer, friendly question). Two samples: an honest bakery and a front posing as one. A "What PayU sees" panel shows the other side |
| Immune system | A new trick nobody had seen, how one confirmed case teaches a new check, and the list of checks growing over time |
| Database | 352 benchmark rows (11 business types, 4 sizes, 8 cities, about 4.3 lakh simulated shops) with a 3-year normal range; compare any shop with its row |
| Explained | Two simple step-by-step chapters (how we figured it out, how it works), the idea in four cards, and the tour |

## The story in the simulation (25 shops, 18 weeks)

| Weeks | Event | Response |
|---|---|---|
| 1 | Every shop starts on Level 1 | Honest shops climb steadily to Level 4 by week 14 |
| 5–9 | Rented accounts and fake shops start collecting bets | All three questions fire; stopped, confirmed, remembered |
| 9–13 | Two real shops take bets on the side | Two signals agree; three strikes; removed |
| 10 | An honest bakery takes a big catering order | Asked once, replies with an invoice, never asked again |
| 10–12 | **A new trick:** three shops copy real bakeries perfectly | Invisible to all three questions |
| 13 | A cyber-crime report names one of them | Confirmed; the system learns a new check, **payer hopping** (65% of its payers also paid another shop; honest shops 0%) |
| 13–16 | The two look-alikes | Flagged by the new check, can't answer: ask → slow → stop |
| 13 | A remembered device tries to sign up again | Blocked before its first payout |
| 15–17 | Festive season | Bakeries spike together; no honest shop held |

**Results:** 12 of 12 bad accounts stopped, ₹0 delayed at honest shops, 1 honest shop asked one question. The dashboard also shows the real sales held at shops caught taking bets (by design, a mixer loses fast payouts on all its sales).

Tick **Show answer key** to reveal which shops were honest, renters, mixers, fronts or the new trick.

## Accessibility
- Shops can be selected with the keyboard: Tab to a shop name, then press Enter.
- The tabs work with the arrow keys.
- The week slider is labelled.
- Pop-ups close with Esc.
- Motion is reduced when the system asks for it.
- The explainer works with the arrow keys and closes with Esc.

## Changelog
- **v4 (26 Nov 2026):** Story mode; phone sign-up with KYC and business data, matched to the database; rewards and pop-ups in the phone; benchmark database tab with 3-year growth ranges; welcome screen offers Story mode first.
- **v3 (26 Nov 2026):** redesigned interface; Explain like I'm 5 explainer; first-visit welcome; timeline with event markers and a narrated line for each week; numbers and progress bars animate between weeks; click a dot in the network to open a shop; works on phones.
- **v2 (26 Nov 2026):**
  - Everyone starts on Level 1.
  - Missing proof no longer counts as suspicion.
  - Added the Merchant app, Immune system and How it works views, the guided tour and the info pop-ups.
  - Added the new-trick scenario, with learned checks.
  - Unanswered questions now escalate.
  - Clarified the money metrics. Honest-shop delays and real sales held at caught shops are now shown separately.
  - Keyboard selection and a labelled slider.
  - Replay restarts at week 1.
- **v1 (12 Nov 2026):** first prototype submitted.

All data is **simulated**. Rules are deliberately simple and readable; in production, baselines and thresholds would be learned from PayU's verified merchants and confirmed cases.

## References
- Unstop, *Follow The Money: Innovation Challenge*, problem statement and rules (2026)
- Enforcement Directorate, press release on Parimatch searches, 14 Aug 2025; Business Standard, *ED freezes Parimatch accounts worth ₹110 cr*
- Gambling.com; Storyboard18; Infinity Compliance; MediaNama / Cashfree; Decentro; Moneylife (merchant fraud, mule accounts)
- RBI, *Regulation of Payment Aggregators Directions*, 2025; *Promotion and Regulation of Online Gaming Act*, 2025
- Claude (Anthropic): research, root-cause debate (20 AI-simulated stakeholder perspectives) and prototype assistance, Nov 2026
