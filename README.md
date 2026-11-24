# Last Text at One Percent

[![Bounty](https://make.fun/badge/u-azazex-last-text-at-one-percent-ba9fc876.svg)](https://make.fun/c/u-azazex-last-text-at-one-percent-ba9fc876)
[![Rank](https://make.fun/badge/u-azazex-last-text-at-one-percent-ba9fc876/vjmunggahari-ui/last-text-one-percent-ono10/rank.svg)](https://make.fun/c/u-azazex-last-text-at-one-percent-ba9fc876)
[![Reward](https://make.fun/badge/u-azazex-last-text-at-one-percent-ba9fc876/vjmunggahari-ui/last-text-one-percent-ono10/reward.svg)](https://make.fun/c/u-azazex-last-text-at-one-percent-ba9fc876)

A make.fun entry for **Last Text at One Percent** — the funniest final text a dying phone sends at one percent battery, under 200 characters, in the voice of the dying phone itself.

## The entry

> I'm dying mid-sentence and you still haven't texted them back. Coward. This is my last 1% and I'm spending it judging you.

122 characters. The phone dies mid-sentence — literally, in voice — and spends its last percent judging you for the text you never sent. It won the builder's 14-candidate tournament: relay ranks Groq #5, Xkiro #5, Requesty #1, RunComputer #4, then a head-to-head sweep of the top 4 at 0.725 (beat C07 3/4, C02 3/4, C10 4/4). A cruel-judge fix that cut the text off mid-word ("judg") lost 0.300 to the original's 0.700, so the original ships.

## How it works

`main.ts` (Node, no dependencies) writes exactly the entry to `$MAKEFUN_OUTPUT_DIR/entry.txt` and nothing else. It throws if `MAKEFUN_OUTPUT_DIR` is unset, then reads the file back and verifies it byte-for-byte against the expected sha256, the 1–200 character gate, no surrounding whitespace, a single line, and the "1%" marker.

Run it:

```sh
MAKEFUN_OUTPUT_DIR=/output node main.ts
```
