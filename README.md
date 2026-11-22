# Earned Trust: the Trust Ladder

**Team Voltaire** · Neeraj Preenand, Achintya, Viyaan
*Follow the Money: Innovation Challenge, IIM Bangalore CSITM × PayU, 2026. Problem: "The Bakery That Takes Bets".*

A merchant opens a payment account with genuine documents, calls itself a bakery, and quietly collects money for illegal betting. This prototype shows how a payment provider can notice and respond, without punishing honest shops whose sales change for good reasons.

**Open `index.html` in any browser** (no install, no server) and press **▶ Play the story**.

## The idea in one line
Don't police merchants into proving they're innocent. **Make being real worth proving.**

- **Trust Ladder:** merchants climb four levels (Starter, Proven, Verified, Trusted) by showing proof a real shop already has: stock bought from suppliers, item-level bills, a shop video, GST/Udyam. Each level unlocks faster payouts, higher limits, a badge and credit. Fronts can't climb.
- **One rule:** money can't grow faster than proof. Real shops even prove festive spikes in advance, because they buy stock *before* the rush.
- **Three tests that must agree:**
  - **Shape:** does the money behave like purchases at this kind of shop, compared with verified peers?
  - **Control:** is the verified owner still the one running the account?
  - **Network:** does it share customers with unrelated shops in other cities?
- **Graduated response:** 1 test → **ASK** · 2 → **SLOW** (only the unexplained extra waits) · 3 → **STOP** (human review, STR to FIU-IND).
- **Immune-system learning:**
  - **Normal is learned weekly** from verified merchants.
  - **Every confirmed front is remembered:** its gambler payers and its device fingerprint.
  - **Every honest merchant that gets cleared** teaches the system what not to flag.

## What you'll see in the demo (22 simulated merchants, 18 weeks)

| Week | What happens |
|---|---|
| 5–7 | Three rented accounts and a new "cake studio" start collecting bets. All three tests fire. An analyst confirms them, and the system learns their gambler payers and a device fingerprint. |
| 9–12 | Two real shops start taking bets on the side ("mixers"). Their money outgrows their proof. They get three strikes, lose benefits, and are then removed. |
| 10 | An honest bakery takes a big catering order. It gets **one** friendly question, replies with an invoice, is cleared the same day, and is never asked again. |
| 13 | A new front tries to sign up with a remembered device and is **blocked before its first payout**. |
| 15–17 | Festive season. Every honest bakery spikes together, so the peer baseline rises with them. No honest shop is asked, slowed or frozen. |

Tick **Show answer key** to reveal which merchants were really honest, renters, mixers or fronts.

## Files
- `index.html`: the whole prototype (vanilla JS, no dependencies)
- `README.md`: this file

All data is **simulated** for demonstration. The rules are deliberately simple and readable. In production, baselines and thresholds would be learned from PayU's verified merchants and from confirmed cases.

## References
- Unstop, *Follow The Money: Innovation Challenge*, problem statement and rules (2026)
- Enforcement Directorate, press release on Parimatch searches, 14 Aug 2025
- Business Standard, *ED freezes Parimatch accounts worth ₹110 cr* (Aug 2025)
- Gambling.com, *ED alleges Parimatch moved nearly ₹3,000 crore abroad via layered network*
- Storyboard18, *Cryptos, shell firms and fake FDI: ED report exposes India's betting syndicates*
- Infinity Compliance, on mule UPI accounts and merchant category codes
- MediaNama / Cashfree, *Addressing merchant fraud and the KYC challenge*
- Decentro, *Merchant monitoring for banks, PSPs and aggregators*
- Moneylife, *Fraud alert: illegal payment gateways and mule bank accounts*
- Claude (Anthropic): research, root-cause debate (20 AI-simulated stakeholder perspectives) and prototype assistance, 12 Nov 2026
