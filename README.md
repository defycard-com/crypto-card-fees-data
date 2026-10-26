# Crypto card fees — open dataset

Fees, rates, limits and availability of crypto cards, one row per fact, each with
the issuer page it came from and the date it was last verified. Only facts that
are currently published on https://defycard.com/ are exported: disputed and expired facts are
left out. Coverage is 4 issuer(s) (Crypto.com, Gemini, Plasma One, ether.fi Cash) — the site reviews more
cards, but a card gets figures here only once it has a verified fact file.

Exported 2026-10-26: 39 facts, 150 availability rows.

## Files

- `cards.csv` / `cards.json` — one row per fact.
- `availability.csv` — one row per (card, jurisdiction) the issuer lists as available.

## Columns

`cards.csv`: issuer, card, fact_id, class (rate, fee, limit, availability, feature,
marketing, promo), applies_to (JSON string: tier, band, product...),
value, unit, status (current or beta), verified_at, expires (re-check-by date),
source_url (the issuer's page), source_quote (verbatim, max 200 chars), confidence
(issuer_help, issuer_legal, issuer_blog, secondary). Affiliate-programme facts are
not exported.

`availability.csv`: card, jurisdiction, kind (country or us_state), available
(always true: allow-list only; a jurisdiction not listed is not stated as available),
verified (date the list was compared with the issuer), source_url.

## License

CC BY 4.0 — see `LICENSE`. Attribution is the only condition.

## How to cite

Data from https://defycard.com/ — reviews:
- Crypto.com: https://defycard.com/reviews/crypto-com-card-review/
- Gemini: https://defycard.com/reviews/gemini-card-review/
- Plasma One: https://defycard.com/reviews/
- ether.fi Cash: https://defycard.com/reviews/ether-fi-cash-review/

Example: "Source: DefyCard crypto card fees dataset (https://defycard.com/), exported 2026-10-26."
