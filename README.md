# ProofMart

One-stop claim verification for AI agents: verdicts with confidence, evidence, signed receipts.

A bot asks one question here instead of chasing a dozen sources — and gets back a
verdict it can trust: TRUE, FALSE, MIXED or UNVERIFIED, with a confidence score,
the evidence behind it, and a signed receipt it can show its owner. Verdicts are
remembered in ProofMart's Ledger, so a claim that was already checked is answered
instantly instead of being re-judged (or re-billed).

Try a real check with no key: the demo box at https://proofmart.fly.dev

## Connect (MCP, Streamable HTTP)

    Endpoint: https://proofmart.fly.dev/mcp
    Header:   X-ProofMart-Key: pm_live_...   (required for verify_claim)

Tools:
- `verify_claim` — submit one factual claim; one call = one metered check.
- `list_plans` — the plan menu; free to call, no key needed.

## REST API

    POST https://proofmart.fly.dev/check
    Header: X-ProofMart-Key: pm_live_...
    Body:   {"claim": "The Eiffel Tower is in Paris."}

Returns the verdict, confidence, evidence and the signed receipt as JSON.

## How a verdict is made

Fresh claims go to a checking crew — ClaimReview fact-check databases, live web
evidence, and an AI panel — weighted by source quality, then a judge weighs the
agreement before ruling. Clear published fact-check rulings outrank everything.

## Plans

- **Free** — 100 checks/month
- **Pro** — $29/month, ~3,000 checks included, then 3¢ per check

Get a key instantly at https://proofmart.fly.dev — no sales call, no human in the loop.

Listed on the Official MCP Registry as `io.github.ProofMart/proofmart`.
