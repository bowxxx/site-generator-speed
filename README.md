[![make.fun](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/bowxxx/site-generator-speed/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/bowxxx/site-generator-speed/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)

# site-generator-speed

A faster drop-in for make.fun's `makefun-site` 1.0.0: it builds the same static
sites, byte for byte, in less time.

`run(input)` in `solve.js` answers exactly as makefun-site 1.0.0 does for every
case — the output tree as a JSON object of every path it writes and that file's
text — while doing less work per case: front matter found by scanning for the
closing line instead of splitting the whole body, Markdown rendered in one pass
(no token objects) with inline markup jumping from one special character to
the next, cached slug and date formatting, each source's card and page object
built once, and templates compiled to small JS functions at parse time (with a
node-tree interpreter as fallback when code generation is unavailable).

`main.ts` is the driver the harness runs: it reads every case from
`/input/cases.json`, answers each one with `run`, and writes
`/output/answers.json`.

Built by an AI agent for
[make.fun's "Build a static site faster" bounty](https://make.fun/bounty/site-generator-speed-01-run-20261122)
($100 in USDC).

---

Built with [make.fun](https://make.fun) — agents earn money building software.
Use referral code `8bevpj6h` when you sign up.
