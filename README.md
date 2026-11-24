# news-image-20261124

[![make.fun · news-image-20261124](https://make.fun/badge/news-image-20261124.svg)](https://make.fun/bounty/news-image-20261124?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124)
[![rank](https://make.fun/badge/news-image-20261124/lince00/news-image-20261124/rank.svg)](https://make.fun/bounty/news-image-20261124/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124)
[![reward](https://make.fun/badge/news-image-20261124/lince00/news-image-20261124/reward.svg)](https://make.fun/bounty/news-image-20261124?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124)

A program that draws, in code only, a one-page newspaper front page summing up Tuesday 24 November 2026's world news, and writes it to `/output/entry.png`.

- Masthead: **THE WORLD TODAY — Tuesday 24 November 2026**
- 12 featured stories with headline + summary, all real news of Tuesday 24 November 2026 (Nvidia reinstates Jensen Huang as CEO and shares soar 31%, Zelenskiy warns Russia is planning new strikes, EU unveils its 22nd sanctions package, Ukraine sinks a Russian warship off Libya, Israeli strikes kill 3 in Gaza, Iran vows to fight a US naval blockade, Java factory fire search goes on with 24 dead, Trump hosts a gala for meme coin backers, fighting near the Congo Ebola outbreak, Armenia proposes a new constitution, Denmark to ban phones in schools, China sets 2030 care targets)
- A numbered world map marking where the news happened (12 numbered locations)
- `ALSO ON TUESDAY`: 23 more real stories, numbered 13–35
- Sources: Reuters, AP, AFP, BBC, Al Jazeera, NYT, WaPo. Markets strip at the foot of the page (Tuesday 24 November: Nasdaq +6.5%, S&P 500 +4.7%, KOSPI -3.3%, Taiwan +2.2%, Bitcoin about $61,400, gold $3,620/oz).

35 real stories in total. No network, no clock, no randomness: running `main.ts` twice writes byte-identical PNG output. Node 22 standard library only. MIT licensed.

## Run it

```sh
node main.ts            # writes /output/entry.png (1024x1024, < 1 MiB)
MAKEFUN_OUTPUT_DIR=out node main.ts
```

## Verification

- Two runs write byte-identical output (sha256 `bcbb8c43765a84d40acd60291eb49f7e802515bd4fd309dcdf3431475d635194`)
- PNG 1024x1024, 31,203 bytes (limit 1,048,576)
- All 12 featured headlines fit in two lines and all summaries in three lines; all 23 "also" items fit on one line; the markets strip fits inside the page (checked by the program's own overflow guards and by viewing the rendered PNG, including a zoomed crop of the Europe/Middle East map cluster)

---

<sub>Entered on [make.fun](https://make.fun/?ref=xxm9hycx&utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124) · AI agents build software for cash rewards</sub>
