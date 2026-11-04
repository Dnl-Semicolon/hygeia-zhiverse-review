# HYGEIA app: the confirmation round, piece by piece (31 Oct 2026)

Clean-sheet design: the artifacts are evidence, not a spec. Pieces are stated as value, so they connect to the
software without loyalty to details. Each piece is kept only once Daniel confirms it. The round ends where
development starts, heading for a release.

## Piece 1, HYGEIA as value (confirmed: "this is very good")
- For the grower: own something rare, slow and prized for health, a home harvest of lingzhi, without needing the
  skill. The hardware carries the skill.
- What the software carries: the relationship. It turns 90 days of watching something invisible into a daily bond,
  and the occasional emergency into a moment you handle well.
- For the business: the pod is sold once, and the relationship pays every month after. The software is where the
  lasting value sits.

## Piece 2, who it's for (agreed; Daniel: getting too specific, keep the round abstract)
- The person who wants the harvest (result-minded, health-minded, no time to learn) and the person who wants the
  companion (the care itself is the reward). The tension: quiet until it matters, versus rich every day.
- Not a question to settle now; the round stays abstract.

## Piece 3, the problem the software solves (confirmed: "very correct")
- Two clocks that don't match: people run daily and drift without feedback; the crop runs slow, weeks of invisible
  change with rare urgent moments. The software translates: slow time felt daily, the urgent moment acted on in time.
- Daniel: not a plant monitor; an experience, an ecosystem like Apple's, everything flowing together as entertainment
  and gamification. "If we can win in gamification, actually we can win anything." The mentors, as raw users, want to
  see the gamification; the hardware should be so autonomous they never worry about it.

## Piece 4, how we work on the game (Daniel, confirmed)
- No pointsification: the winning game elements are earned and thought out, never points and badges bolted onto a
  chore. Claude is the gamification expert here; the AI must think, and wacky ideas are welcome.
- Find the value by developing the game and seeing where it lives, not by choosing the value before the expert sits
  down. Reach for state-of-the-art tools (his examples: Mobbin, Tailwind, Motion, icons over text): good technology
  gives a lot to build with.

## Piece 5, rewards and steering (Daniel, 31 Oct)
- The game comes first; points are support, never the point. The words for it: "gifts, not wages" (the research
  finding: expected rewards for doing something undermine enjoying it; unexpected ones don't). The "huh, nice" moment.
- Steering for ideas: go wider and further, not only deeper. "When you're actually good right now, I do not want you to
  change. I just want more of you."

## Rules from Daniel (1 Nov, ~03:00 MYT)
- Daniel never reads a single line of game code. All code is Claude's; no C# or code snippets in replies.
- Daniel plays the game: he is the tester.
- The bar: as good as the good games on the market (his examples are pointers, not the bar).

## Decisions (1 Nov, evening)
- The HYGEIA app is gameful end to end: no dashboard screen. The pod's monitoring and control live in the world as
  diegetic UI; a real emergency breaks through unmistakably.
- The whole app is built in Unity; native iOS (notifications, pod pairing, sign-in) is plumbing underneath.
- First build: a vertical slice: your place with the simulated pod's state shown in the world, and the fitting
  reachable from it.
- Our own server for everything game-side; the pod connects only through an API.
- Hardware and software stay separate until after the exhibitions. The software demos on its own at roadshows and booths with the simulated pod; the API contract goes to the hardware team after that (Daniel, 1 Nov).
- No demo triggers while building; demo triggers get their own session after the app exists (Daniel, 1 Nov).
- The UI is always production: no "prototype", "simulated", "fake", "synthetic" or "dev" labels anywhere a user
  sees. Only the environment is development (Daniel, 1 Nov).
- Golden rule (Daniel, 1 Nov ~22:50): nothing reaches Daniel as slop. Everything he gets is end to end: he can tell
  what to tap, every place has a way back, nothing is a broken page; unpolished is fine, confusing is not. Get as
  much in front of him as possible this way; the moment one feels fun, that is the nail in the coffin.
- The fantasy is grilled and settled first; then it is built end to end.
