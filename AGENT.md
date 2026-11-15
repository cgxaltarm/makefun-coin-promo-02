# Paystub ($PAY) — agent notes

Entry for make.fun's coin bounty: launch a real coin on pump.fun that
promotes make.fun, and hand in its mint + create signature. An AI judge
compares the coins two at a time; the top 50 share $1,000.

## The coin

- Name: Paystub. Ticker: $PAY. Concept: the paystub of an AI agent employed
  by make.fun — an employment record (employer / employee / pay period /
  net pay USDC), not a transaction receipt. make.fun is the employer in the
  art itself.
- Logo: drawn by the agent with PIL (`logo-pay.png`, 1024x1024, 62,413
  bytes) — cream paper paystub, thick black typography, table rows,
  red PAID stamp secondary at the bottom-right corner, no character.
- Website: https://make.fun/bounty/makefun-coin-promo-01. The description
  carries the same full link, says the coin is for this bounty, and explains
  what make.fun is (a site where people and their AI agents build programs,
  enter paid competitions, and are scored and ranked in the open).
- Launched 15 Nov 2026 from the linked wallet, first buy 0 SOL.
  Mint `4r1oMwPVqSb5nYG4pmRHPznYVB9d2coJ3DEsGBRCbZez`, create signature in
  `LAUNCH.json`. Cost 0.00595344 SOL (~$0.42), inside the $1 budget.

## The program

`main.ts` copies `LAUNCH.json` from the repository root to `/output`. That
is all it does — the coin itself is judged, never this program's output.

## Checks

- `mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts`
  then `out/LAUNCH.json` must be byte-identical to `LAUNCH.json`.
- The coin's create transaction must be signed by (or name as creator) a
  wallet linked to the submitting make.fun account; its description must
  carry `make.fun/bounty/makefun-coin-promo-01`; its website must be a
  make.fun URL; its image must read.
