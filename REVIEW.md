# App Lab — 5 Playable Prototypes

**Built:** June 30, 2026 (overnight batch run) · **Status:** all 5 playable, self-tested, ready for your review

Hi Taylor — while you were out I researched what makes casual games stick, then designed, built, and tested 5 fresh prototypes. Each is a single HTML file you can double-click to open in any browser. They work fully offline, save nothing but a high score on your own device, and have sound + a mute button. Nothing here duplicates your two existing apps (the 2-player "settle a score" game or the group decider).

**How to try them:** open any folder below and double-click `index.html`. They're built mobile-first, so they look best in a narrow window or on your phone — but they work fine on desktop too. Tap to play; press the 🔊 in the top corner to mute.

---

## What the research said (and how I used it)

A few findings shaped every prototype:

**The first 10 seconds decide everything.** Casual players learn by doing, not by reading. Tutorials kill retention — one source notes only ~18% of users stick with a steep first session vs ~41% with gentle, learn-by-playing onboarding. So every app here teaches itself through one obvious action, with a one-line prompt and no tutorial screen.

**The core loop must be short and instantly repeatable.** Good casual sessions are seconds-to-minutes long, with success/failure that's instant and clear, and a "tap to try again" that's always one button away. All 5 use a tight loop: act → immediate feedback → score → retry.

**"Juice" is what makes it feel good** — the pop, the screen shake, the particle burst, the rising pitch on a combo. It's the felt connection between your tap and the game's response. I added generated sound (no audio files), haptics, particles, and win animations to every app. The research also warns juice can *mask* a weak game, so I made sure each loop is fun even with sound off and motion reduced.

**Difficulty should start near-impossible-to-fail and ramp gently.** Early wins hook people; the challenge rises as they improve. Each app ramps: the reflex target shrinks, the tower slab speeds up, the memory sequence grows, etc.

**What flops:** steep learning curves, no feedback, difficulty spikes, and juice with no substance underneath. I aimed to avoid all four.

### Sources
- [What Are Hyper-Casual Games? Trends, Psychology & Business in 2025 — Exscape](https://exscape.com/what-are-hyper-casual-games-trends-psychology-business-in-2025/)
- [How to Develop Hyper Casual Games: A Beginner's Guide (2025) — GameSD](https://www.gamesd.app/guide/how-to-develop-hyper-casual-games-for-beginners)
- [How to Build Profitable Hyper-Casual Games 2025 — Gamixlabs](https://gamixlabs.com/blog/how-to-build-profitable-hyper-casual-games-2025/)
- [Making a Hyper-Casual Game? 5 Common Mistakes to Avoid — GameAnalytics](https://www.gameanalytics.com/blog/hyper-casual-game-common-mistakes)
- [Retention through Metrics: Challenges, Engagements & Progression — Riseup Labs](https://riseuplabs.com/game-retention-metrics/)
- [How to Design Games for Retention | Game UX Tips — Pixelfield](https://pixelfield.co.uk/blog/how-to-design-games-for-retention/)
- [Mobile Game Onboarding: UX Strategies That Boost Retention — Medium](https://medium.com/@amol346bhalerao/mobile-game-onboarding-top-ux-strategies-that-boost-retention-6ef266f433cb)
- [Juice in Game Design: Making Your Games Feel Amazing — Blood Moon Interactive](https://www.bloodmooninteractive.com/articles/juice.html)
- [The "Juice" Problem: How Exaggerated Feedback is Harming Game Design — Wayline](https://www.wayline.io/blog/the-juice-problem-how-exaggerated-feedback-is-harming-game-design)
- [Squeezing more juice out of your game design — GameAnalytics](https://www.gameanalytics.com/blog/squeezing-more-juice-out-of-your-game-design)

---

## The 5 prototypes

I deliberately spread these across genres and moods: a reflex twitch game, a word game, a number puzzle, a spatial timing game, and a memory game — a mix of fast vs calm and skill vs pattern.

### 1. Reflex Ring — *reflex / timing*
**Hook:** Tap the instant the glowing dot crosses the mint zone. One miss ends the run.
**How to play:** A dot sweeps around a ring. Tap (anywhere, or Space) while it overlaps the mint target arc. Every hit shrinks the target and speeds up the dot, and the direction flips every few hits.
**Why it should work:** Pure one-tap loop, zero instructions needed, instant fail/retry, and a difficulty curve that tightens automatically — a textbook "easy to start, hard to master" score-chaser.
**Tested:** Boots clean; hit-on-target scores, miss ends the run, target shrinks as score rises. ✓
**Folder:** `reflex-ring/index.html`

### 2. Jumbl — *words*
**Hook:** Unscramble the word before the clock runs out; keep your streak alive.
**How to play:** A scrambled word appears with a hint. Tap letter tiles to spell it (or type on a keyboard). Solve it and the next one appears instantly. 90-second sprint; longer words + streaks score more; a Hint button reveals the next letter for a 3-second cost.
**Why it should work:** Word games have broad, durable appeal and a calmer pace than reflex games — good genre variety. The streak + timer create tension and replayability, and the embedded word bank means it works 100% offline with no dictionary file to download.
**Tested:** Boots clean; word bank is all clean A–Z entries with hints; scramble always uses the exact letters of the answer; solving increases score and streak. ✓
**Folder:** `word-sprint/index.html`
**Open question for you:** the bank is ~50 hand-picked words. Fun for a demo, but you'd want a few hundred before launch — easy to expand.

### 3. Make Ten — *numbers / puzzle*
**Hook:** Tap a chain of touching numbers that adds up to exactly 10 to clear them.
**How to play:** On a 5×6 grid of digits, tap touching cells to build a running sum. Hit exactly 10 and the chain clears; new numbers drop in from the top. Overshoot 10 and the chain resets. Chain quickly for combo multipliers. 60-second sprint.
**Why it should work:** Light mental-math puzzle with a satisfying clear-and-refill loop (the same dopamine as match-3). Calm but with a timer for pressure; combos reward skill, so there's a mastery ceiling.
**Tested:** Boots clean; a 4+6 chain scores, an over-10 chain (9+9) scores nothing and resets, and the board stays full after cells collapse and refill. ✓
**Folder:** `make-ten/index.html`

### 4. Tower Stack — *spatial / timing*
**Hook:** Drop the sliding slab onto the stack — overhang gets sliced off.
**How to play:** A slab slides across the top; tap to drop it. Whatever hangs past the edge below is cut away, so the tower narrows as you go. Nail a perfect alignment and you keep full width + a bonus. Miss the stack entirely and it topples. The camera pans up as you climb; speed rises with height.
**Why it should work:** A proven, intuitive arcade mechanic (one tap, instantly understood) with a beautiful tension: every drop is a small risk, and "perfect" stacks feel great with the rising-pitch chime. Strong juice payoff.
**Tested:** Boots clean; perfect drop keeps full width and increments height + perfect counter; partial overlap trims the slab and resets the perfect streak; a total miss ends the game. ✓
**Folder:** `tower-stack/index.html`

### 5. Echo — *memory*
**Hook:** Watch the glowing pattern, then tap it back from memory.
**How to play:** The four colored pads light up in a growing sequence, each playing a musical note. Repeat the sequence by tapping (or keys 1–4). Each round adds one step and the melody grows. One wrong tap ends the run.
**Why it should work:** The Simon mechanic is timeless and needs no explanation. The twist is musicality — the pads are tuned to a pentatonic scale, so every sequence sounds pleasant, which makes the memory work feel rewarding rather than dry. Calm, satisfying, very different mood from the reflex games.
**Tested:** Boots clean; four pentatonic notes defined; round 1 generates a 1-step sequence; all sequence values are valid pad indices. ✓
**Folder:** `echo-memory/index.html`

---

## How I tested (so you can trust "it works")

I ran an automated harness in Node that stubs out the browser (DOM, Web Audio, localStorage, etc.), extracts each game's script, and confirms it **boots with no errors**. Then a second script **drives the actual game logic** and checks the rules hold. Results:

- **Static checks (all 5 × 10 = 50 checks): all passed** — viewport meta present, no external/internet dependencies, reduced-motion handled, mute toggle present, on-device storage only, haptics present, Web Audio (no audio files), 44px+ tap targets.
- **Behavioral logic (28 checks): all 28 passed** — win/lose/scoring/edge cases for every game (e.g. Make Ten correctly rejects an over-10 chain; Tower Stack ends on a total miss; Reflex Ring ends on a mistimed tap).

What the automated tests **can't** fully judge is *feel* — whether the speeds, timings, and animations are fun. That's where your hands-on play comes in.

---

## My ranking (most to least promising)

1. **Tower Stack** — the most universally graspable and the most satisfying "juice" payoff per tap. Best instant-demo appeal and the clearest path to "one more try."
2. **Reflex Ring** — dead simple, genuinely tense, great for short bursts. Slightly less novel than Tower Stack but very polished as a score-chaser.
3. **Make Ten** — strongest *depth* and longest potential session; the combo system gives it a skill ceiling. Slightly slower to "get" than the top two.
4. **Jumbl** — broad appeal and a nice change of pace, but needs a bigger word bank before it feels deep, and word games are a crowded space.
5. **Echo** — lovely and calming, but it's the most familiar mechanic (Simon) and has the lowest novelty, so it's the hardest to stand out with.

This ranking is about *commercial stickiness*, not quality — all five are clean and playable. If you just want the most *relaxing* one, Echo and Make Ten lead.

---

## Legal / Privacy note

- **No data is collected.** Every app stores only a high score and your mute preference in your browser's local storage, on your device. There are no accounts, no network calls, no analytics, and no tracking. I verified "no internet dependencies" as part of testing.
- These are **general-audience casual apps**, not children's apps — no kid-targeting, nothing for the App Store "Kids" category, consistent with steering clear of COPPA's strictest rules.
- **Before you ever take money or collect anything** (an email, a leaderboard, an ad SDK, a purchase) — even something that seems harmless — please get a real lawyer's review. Ad networks and analytics SDKs in particular often collect data on your behalf, which changes your privacy obligations. Nothing here crosses that line yet, and I'd flag it loudly before it does.

---

## Next steps — what you can approve, kill, or tweak

When you're back, play them and tell me in plain language. Some concrete decisions you could make:

- **Pick 1–2 favorites** to develop further (I'd nominate Tower Stack + one other). We go deep on those rather than spreading thin.
- **Kill any that don't click** for you — no attachment, that's what prototypes are for.
- **Request feel tweaks** on any of them: "the dot's too fast," "the timer's too short," "make the perfect-stack effect bigger," "I want it calmer/punchier." Feel is exactly the thing I can't test automatically, so your reactions drive the next round.
- **Direction calls I'd love your input on:** Should any of these get a daily-challenge or simple progression (levels, unlockable color themes)? Should Jumbl get a bigger word bank now or later? Do you want a shared visual identity across an "arcade" of mini-games, or distinct looks per app?

Notes on choices I made autonomously (since you weren't here to ask): I picked the 5 genres for maximum variety; set session lengths (90s for Jumbl, 60s for Make Ten) as reasonable defaults; and kept tiny `__RR__`/`__JB__`/etc. test hooks in the code (harmless, no data, they just make future automated testing easier — I can strip them anytime).

— Your dev & design partner
