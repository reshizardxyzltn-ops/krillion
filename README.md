# One in a Krillion: Highlander Edition

A rarity trivia game for *The Highlander*. Players get seven prompts with 25 seconds each. Any correct answer counts, but the rarer the answer, the deeper the sub dives, from the surface down to the trench floor at 7,000 m.

It's one self-contained `index.html` with no build step and no dependencies. Fonts load from Google Fonts. Sounds are made in the browser.

## Prompts

1. A public high school in Northern Virginia
2. An AP class
3. A candidate who ran in the 2026 U.S. Senate election
4. A country with blue in its flag
5. A board game released after the year 2000
6. An over-the-counter medicine
7. A liberal arts college or university

## Scoring

| Tier | Points | Depth |
|---|---|---|
| Plankton | 10 | 100 m |
| Too Clever | 15 | 150 m |
| Schooler | 30 | 300 m |
| Rare | 60 | 600 m |
| Deep Cut | 85 | 850 m |
| One in a Krillion | 100 | 1,000 m |

The best possible score is 700 points, which takes you to 7,000 m.

## Answer matching

- Capitalization, punctuation and accents are ignored. Common extra words like "High School", "AP" and "College" are dropped before matching.
- Nicknames work, for example APUSH, TJ, W&M and Pepto. Last names work for Senate candidates.
- Answers with extra words still count, for example "Ticket to Ride Europe" or "Children's Tylenol".
- Typos and partial answers get a **"Did you mean…?"** question with up to 3 choices. The timer pauses while it's showing.
- Common wrong answers get their own message, for example "Catan: released 1995, too early!".

The full word bank only appears at the end of a game.

## Run it locally

Open `index.html` in any browser. That's it.

## Put it online with GitHub Pages

1. Create a new repository on GitHub and upload the files from this folder (`index.html`, `README.md`, `.nojekyll`).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, and click **Save**.
4. After a minute the game will be live at `https://<your-username>.github.io/<repo-name>/`.

## Editing the word bank

All answers live in the `CATS` array inside the `<script id="logic">` block in `index.html`. Each category has six tier lists (`plankton`, `clever`, `schooler`, `rare`, `deep`, `krill`). Every answer is one line:

```
Display Name|alias one|alias two#Optional note shown after a match
```

- Aliases are extra spellings that also count.
- Start a line with `=` to stop the game from dropping generic words like "college" from that answer. Use it when the shorter name would clash with something else, as in `=Colorado College`.
- `nope` lists common wrong answers and the message each one gets.
- `hint` is the small line under each prompt.

To change a prompt, edit its `prompt` text and replace its tier lists.

## Credits

Built for *The Highlander*. The game format is inspired by Krillion ([krillion.io](https://krillion.io)). This edition is not affiliated with it, and all of its art and text are original.
