# Golden rules for building ZhiVerse (Daniel, 1 Nov 2026)

How the agent loop runs. Each rule names the table stake (`Table stakes.md`) or the goal it protects; the rules on
how to talk to Daniel live in `~/reading-room/CLAUDE.md`, not here.

1. Settle the fantasy before the verb, and the verb before the art. Protects: fun.
2. Design top-down from `ZhiVerse map.md`; never anchor on a first screen or polish a throwaway. Protects: fun, speed.
3. Fun is the only test. Get as much in front of Daniel as possible; the moment one feels fun, that is the one.
4. Ready-made art first; Blender only for what nobody sells (the lingzhi). Pick from references. Protects: speed.
5. The UI is always production: no "simulated", "prototype", "dev" labels, no demo triggers. Protects: the HIG.
6. Anything that can use the GPU uses it. Protects: speed.
7. Measure change to phone (`~/code/hygeia-zhiverse/ship.sh`, baseline 123 s) and drive it down. Protects: speed.
8. No checker for now: Daniel is the only judge, of small end-to-end batches, so a bad batch costs a day, not a week.
   A checker earns its place once there is something good to protect (Daniel, 1 Nov: "can"). Human on the loop, not
   in it: he is called only for a build worth playing or a decision only he can make. Protects: Daniel's time.
9. What can be counted is counted every build and only goes down (tap targets under 44 pt, screens with no way out,
   text under 11 pt). Protects: the table stakes.
10. Before building any moment, and before settling the fantasy, read HYGEIA's own artifacts first (the decks, the team's
    videos), then study how three or more great games already do it
    (Game UI Database screens, first-ten-minutes recordings as contact sheets) and build from the best pattern: no
    hand-rolling from imagination, no gold plating, no table stake left out. Borrow patterns for moments, never a
    whole game (Daniel, 1 Nov: "a gold mine of intelligence").
11. Undecided big choices (the fantasy first) ship as two or three thin end-to-end slices on Daniel's phone at once,
    each explaining itself through play, no pitch; he keeps the one that feels like a game (set-based design).
12. Media reaches the main thread as media. Agents fetch and label images, recordings and pages, and never describe
    them in place of the thing; I look at the source myself (Daniel, 1 Nov: describing screens "is distillation").
13. Idle hardware while building or rendering is a red flag (Daniel watches Mikoshi's monitor, port 8090, over an
    hour): the bottleneck must never sit idle (Goldratt). Deciding and writing use no GPU and shouldn't; keeping
    everything busy for its own sake is waste.
14. Pitches are previz: made in the real engine with the real assets (Unity, Blender), showing play, never text
    slides, so whatever Daniel likes goes straight into the app (Daniel, 2 Nov: "the video has no loyalty towards
    what is going to be shipped"; a text survey of choices is death by PowerPoint). Previz is kitbashed from what
    already exists (Kenney packs, the Unity scenes, the one lingzhi we have); new art is made only after Daniel backs
    the previz (Daniel, 2 Nov: Blender from scratch first is "work commissioned before the backing from me").
15. Evidence, not guesses: every design claim carries its source (a quote, a file, a result) or says "guess"; a guess
    gets its cheapest real check (a spike: run it, look at it, play it) before anything is built on it.
16. When asked to design the app icon, be bold, and keep minimalism out of mind: it is earned, not a starting point.
    Nobody has decided what the icon is yet, so work from references and Daniel's say, never from my assumptions
    (Daniel, 3 Nov: "you didnt know what to have as the icon, you only worked on assumptions. but you will be asked to
    be bold and make a chnage, when you do, dont include minimalism in your mind"; earlier that day: "the icon must be
    fucking beautful not just a mushroom"). Source: Mark Omlor, Brand Designer, reel `sources/ig-DfISImis7yM/`
    (transcript `reel.txt`): "Simplify after you're known, not to get known." Protects: recognition at the booth.
