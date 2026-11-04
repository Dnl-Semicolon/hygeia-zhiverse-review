# Completeness matrix: how much of five games Hygeia provides (4 Nov 2026, 08:02 MYT)

Daniel's words (4 Nov, 07:5x): "why don't you understand the game fully and then try to pull in every single thing about every single game and then try to emulate it and then judge yourself for completeness ... the thing to measure is that you look at a game and then you read its documentation and then read everything it's able to support. ... and then you measure it against yourself and then see how much you actually provide to them."

Built against: `~/code/hz-skeleton/three/src` at commit bebf19b (read only; another agent edits it, so the numbers move) and the screens `/tmp/hz-outside/*` and `/tmp/zhiverse-skeleton/*` (rendered 3 Nov 23:56 UTC). Fun is not scored: Daniel judges it.

## 1. The number, one per game

Score = (has + half of partly) / capabilities that apply. Not-for-us rows leave the denominator; each carries a one-line reason. Re-score by changing a row's status in section 4, then recount; the number should only go up.

| Game | Provided / applies | Score | has | partly | missing | not-for-us |
| --- | --- | --- | --- | --- | --- | --- |
| Clash Royale | 11 / 42 | 26% | 6 | 10 | 26 | 5 |
| Clash of Clans | 5.5 / 29 | 19% | 1 | 9 | 19 | 3 |
| Pokemon Sleep | 7 / 26 | 27% | 4 | 6 | 16 | 3 |
| Finch | 6 / 16 | 38% | 5 | 2 | 9 | 3 |
| Honkai Star Rail | 5 / 25 | 20% | 1 | 8 | 16 | 7 |
| All five | 34.5 / 138 | 25% | 17 | 35 | 86 | 21 |

Rules so the number can only be climbed honestly (the lesson of `sources/how-we-made-claude-ai-faster.html`: a metric has two jobs, "a metric Claude could move in the lab" and "a guardrail ... with a number that could only ratchet", and one that "didn't actually correlate" with what users feel is thrown out):
- A row moves to `has` only when its evidence is a screen or a file a reader can open, not a plan. `partly` is worth half.
- A row moves to `not-for-us` only on Daniel's say. Otherwise the denominator shrinks and the number rises for free (Goodhart's law: a measure that becomes the target stops measuring; the lesson people took is to pair it with a check from outside the number, and the pushback here is that 100% of Honkai Star Rail would be a different product, so no game's number is a target to reach, only a map of what is not yet there).
- Guess, not yet checked: that this number tracks what a person holding the app for two minutes feels. The cheapest check is section 2 against the booth: watch whether the people who stall are stalling on the missing rows at the top of that list.
- The five games' lists are not equally deep. Fandom, Bulbapedia, Prydwen, HoYoWiki and Finch's help centre sit behind a bot check and returned nothing, so Finch (16) and Honkai Star Rail (25) rest on store pages, Wikipedia, Game8's index and the coworker interview, and are thinner than Clash Royale (42). Their denominators will grow when someone reads more.

## 2. The 15 missing capabilities that matter most to someone holding the app for two minutes at a booth

Most important first. Every one is a `missing` row in section 4. "His complaint" cites `hygeia/company/demon/BUGS-HE-SAID.md` (compiled 2 Nov 07:15, so some rows may since be fixed).

1. **Where you stand, on the home screen** (Clash Royale, row "Home shows where you stand"). Clash Royale's home shows your arena and trophy count, so a stranger sees at once that there is a place to climb to. Hygeia's home (iphone-1-first.png) shows five readings and a button, nothing about the player. His complaint: #28 "What is this day 48 and then the top left?"; #49 too much empty space.
2. **A guide who speaks first** (Pokemon Sleep, "Professor Neroli gives you a Snorlax"; Honkai Star Rail companions). A named character who frames the world in the first ten seconds, instead of one hint line ("Hold your light on a puff"). His complaint: #23 "there are no NPCs".
3. **Sound, music and voice** (Pokemon Sleep: "Pokémon-inspired music"; Honkai Star Rail: original score and four-language voice-over). Hygeia has no audio at all (grep: only the dev voice channel uses it). Guess: a noisy roadshow hall mutes much of it, so this is first-ten-seconds mood more than instruction. No complaint of his about sound is in the file.
4. **A live person across the table** (Clash Royale: live 1v1 and 2v2). Two visitors side by side playing each other or together; Hygeia's duels are against saved teams and the 2v2-like borrow-a-lantern is unreachable from the Friends tab. His complaints: #30 "the robots too much better than me", #23 "in clans you don't walk around you just click".
5. **A board to beat** (Clash Royale global tournaments and leaderboards; Clash of Clans Legend League). A visible ranking of the booth's own visitors gives the second minute a reason. Today Friends lists four hard-coded neighbours (village.ts KEEPERS).
6. **Something happening now** (Clash Royale news and season card; Pokemon Sleep "New Moon Day #19"; Finch "Hidden Hollow ... Ends on 11/29"). One card on the home that says tonight is different. Hygeia has no events, news or season.
7. **A reason to come back tomorrow** (Pokemon Sleep's day cycle and morning report; Finch's streaks and morning and evening check-ins). The two-minute visitor asks "and then?". Hygeia has no daily rhythm; "since you were here" exists (home.ts sinceLine) but is not on the home.
8. **Choose before you play** (Clash Royale: 8 of your cards, hand of 4). Gives agency in the first minute; Hygeia's three helpers are fixed. His complaint to weigh against it: #4 "there's no hicks law here at all" and #26 "too many options", so keep the choice to a pick of three.
9. **Spend something to get stronger** (Clash Royale card upgrades; Clash of Clans Laboratory). A reason to care about the next night. Hygeia's lingzhi are only unlocked and worn.
10. **A named currency you earn** (Honkai Star Rail "Stellar Jade ... earned through gameplay"; Clash Royale elixir). His complaint: #29 "what the fuck is a dew? Why don't we just use elixir". Hygeia's glow is the only resource and it vanishes after the night.
11. **Auto-play for the lazy minute** (Honkai Star Rail auto-battle and fast-forward). The coworker interview (00:16-00:23): "Auto-Pilot game ... You just start with the auto everything". Hygeia is manual only.
12. **A star rating for each night** (Clash of Clans three-star scale). One glance for "how did I do"; the game-over card shows waves and puffs only (keeper/main.ts:455).
13. **A story the pet brings back** (Finch: "back from adventures to share stories"). Something warm to open to; nothing returns to the Pod while you are away.
14. **Help, privacy and terms inside the app** (Clash Royale and Clash of Clans: Settings > Help and Support, privacy, parent's guide). Settings holds only a vibrate switch, the account rows and Delete. Guess: Apple review and any visitor who wants to know what the pod sends will look for these. His complaint: #51 "the settings page is still shit".
15. **Notifications with a stated reason** (Clash Royale optional notification permission; Pokemon Sleep morning). Needed for item 7 to work; nothing asked today.

Left out on purpose: medals and counts (Daniel, 2 Nov 07:3x, me.ts line 4: "don't serve any purpose and are taking screen real state"), so the coded-but-hidden achievements are `not-for-us`, not missing. His #50 "these are meant to be progressions" says the opposite about unclickable medals; that is open for him to settle.

## 3. Sources, downloaded to `~/reading-room/hygeia/company/completeness/sources/`

| Code | File | What |
| --- | --- | --- |
| CR-AS, COC-AS, HSR-AS, FI-AS | `cr-appstore.html`, `coc-appstore.html`, `hsr-appstore.html`, `finch-appstore.html` (+ `*-itunes.json`, text in `*.txt`) | Apple App Store page: description, in-app purchase list, release notes |
| PS-AS | `ps-itunes.json` (id 1579464667; the lookup by the old id returned nothing) | Pokemon Sleep App Store listing |
| CR-WP, COC-WP, HSR-WP | `cr-wikipedia.html`, `coc-wikipedia.html`, `hsr-wikipedia.html` | Wikipedia, second best |
| PS-WP | `ps-wikipedia.html` | Wikipedia |
| CR-SC | `cr-supercell.html` (= `cr-site.html`) | Supercell's game page |
| PS-OFF | `ps-official.html`, `ps-pokemon.html`, `ps-devices.html`, `ps-news.html` | The Pokémon Company's site (sleep-tracking, extra-content and FAQ pages came back as the same shell) |
| PS-PLAY, FI-PLAY, HSR-PLAY | `ps-play.html`, `finch-play.html`, `hsr-play.html` | Google Play pages |
| PS-G8, HSR-G8 | `ps-game8.html`, `hsr-game8.html` | Game8 guide index (a fan wiki, second best), used for feature names only |
| coworker | `~/reading-room/hygeia/interviews/2026-11-02-coworkers/what-gamers-expect.txt` | Colleagues on Honkai Star Rail, "ZenZenZen" (guess: Zenless Zone Zero), Genshin, gacha |
| BUGS | `~/reading-room/hygeia/company/demon/BUGS-HE-SAID.md` | His complaints, numbered |

Blocked by a bot check (the files hold a "Just a moment" page, not content): `cr-wiki-*.html`, `coc-wiki.html`, `hsr-wiki.html`, `ps-bulba.html`, `hsr-gg.html`, `hsr-prydwen.html`, `finch-help.html`, `finch-faq.html`, `finch-fandom.html`, `cr-royaleapi.html`, `hsr-fandom2.html`. `hsr-hoyoverse.html` and `hsr-site.html` are a JavaScript shell with no text. Not used as facts.

Hygeia evidence shorthand: file paths are under `~/code/hz-skeleton/three/src/`; screens are `/tmp/hz-outside/iphone-N-*.png` (1 first, 2 friends, 3 me, 4 pod-tap, 5 play) and `/tmp/zhiverse-skeleton/` (3-night, 4-delete, 5-dashboard). "Guess" marks where only absence in a grep was checked.

## 4. The rows

Status: has / partly / missing / not-for-us. Hygeia's own: the pod's real readings drive growth (Pokemon Sleep and Finch have the nearest ideas), haptics on every action (app/native/haptics.ts, on/off in Settings), guest play before any account (shell.ts), delete-my-progress. These are not counted: no game's list asked for them.

## Clash Royale


### Home screen

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Start a battle in one tap from the home screen | CR-AS "Start battling against players from around the world" | has | Guard-your-lingzhi button, /tmp/hz-outside/iphone-1-first.png |
| Home shows where you stand (arena, trophies) | CR-WP Gameplay: "progress through a series of themed arenas" | missing | iphone-1-first.png shows readings only, no rank (BUGS #28 "What is this day 48") |
| In-game News section for what is new | CR-SC "keep an eye on the in-game News section" | missing | none in app/home.ts, app/app.ts (grep) |
| Home restyled for the season (new season card, tower skins) | CR-AS "NEW SEASON" card; "Tower Skins" | missing | no seasonal code (grep season) |

### Core loop

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A match lasts about three minutes and has a clear end | CR-WP "Battles last up to three minutes" | has | games/keeper/sim.ts K.nightSecs=180, dawn win |
| Spend a resource that refills (elixir) to play units | CR-WP "elixir ... up to 10" | partly | glow gates helpers (sim.ts K.helpers cost; iphone-5-play.png) but it comes from popping puffs, not from time |
| Drag a card from your hand onto the field | CR-WP "Cards are deployed onto the arena" | has | keeper/main.ts:317-326 drag-to-place; iphone-5-play.png |
| A hand of 4 cards cycling from a deck of 8 | CR-WP "deck of eight cards, four ... in hand" | missing | three fixed buttons Jar/Helper/Lamp (keeper/main.ts:266-268) |
| Card types: troops, buildings, spells | CR-WP | partly | three helper kinds only (sim.ts K.helpers) |
| Destroy enemy towers while defending your own | CR-WP | partly | defend only: lingzhi has 100 hp (iphone-5-play.png) |
| Pressure rises late in the match (double elixir, overtime) | CR-WP "elixir generation doubling" | partly | each wave 12% faster (sim.ts K.faster); no overtime |
| Match against a live human | CR-WP "real-time multiplayer" | missing | keeper is solo; Walk duels use saved teams, not live (village/world.ts) |
| 2v2 with a friend | CR-WP "cooperative 2v2 mode" | missing | borrow-a-lantern code still in keeper/main.ts (lent) but the Friends tab no longer offers it (iphone-2-friends.png) |

### Progression

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Trophies unlock new arenas and cards | CR-WP | missing | app/store.ts holds waves best only |
| Ranked leagues up to Ultimate Champion | CR-WP; CR-AS "League and Global Tournaments" | missing | none |
| Account level that rises as you upgrade (King level) | CR-WP | missing | none |
| Upgrade a card with duplicates and gold | CR-WP | missing | none |
| Monthly season with a reset and rewards | CR-WP "monthly seasons" | missing | none |
| Personal best remembered and celebrated | CR-SC "win Trophies, Crowns and glory" | has | keeper/main.ts:455 "Your best yet!" |

### Collection

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Collect 100+ cards you can browse | CR-AS "COLLECT AND UPGRADE 100+ CARDS" | partly | 6 lingzhi (app/kinds.ts) + 8 lore cards in Walk (village/world.ts CARDS) = 14; Me shelf iphone-3-me.png |
| Rarity tiers (common, rare, epic, legendary, champion) | CR-WP | missing | the six lingzhi are colours earned differently (kinds.ts), not tiers |
| Build a deck: pick 8 from your collection | CR-WP | missing | the lingzhi you wear changes the Pod only (me.ts card) |
| Evolved or hero form of a card | CR-WP "Card Evolutions", "Heroes" | missing | none |
| Cosmetic skins for your towers | CR-AS "Tower Skins" | partly | wear one of six lingzhi on your Pod (store.ts wear; me.ts) |
| Emotes | CR-AS "Emotes" | missing | none |

### Rewards

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A reward after each match (chests) | CR-WP | partly | a new lingzhi appears on the game-over card when its challenge is met (keeper/main.ts:455), nothing otherwise |
| Challenges with a goal and a prize | CR-WP "challenges ... reward players based on wins" | partly | each lingzhi has a one-time challenge (kinds.ts how); none repeat or rotate |

### Social

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Join or form a clan | CR-AS "JOIN A CLAN" | missing | none |
| Request and donate cards inside a clan | CR-AS "share Cards" | missing | none (borrow-a-lantern unreachable, see 2v2) |
| Clan Wars | CR-AS; CR-WP | missing | none |
| Global tournaments and leaderboards | CR-AS | missing | Friends shows others' best waves for signed-in households only (app/village.ts loadOthers); no board |
| A friends list | CR-AS "Supports Game Center ... play with friends" | partly | iphone-2-friends.png: four hard-coded neighbours (village.ts KEEPERS) plus server households when signed in |
| In-game chat | CR-AS "Contains Messaging and Chat" | not-for-us | open chat with strangers needs moderation; wrong for a 2-minute booth |

### Story and events

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Seasonal events and themed challenges | CR-AS "SEASONAL EVENTS" | missing | none |
| Limited-time modes (Retro Royale, Goblin Queen) | CR-WP | missing | none |
| A second permanent mode (Merge Tactics) | CR-WP "July 2025 ... permanent game mode" | partly | Walk the village, reached from Friends (app/modes.ts MODES has one entry) |

### Onboarding

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Short sessions that fit a pocket moment (3 to 5 minutes) | CR-WP | has | a night is 3 minutes (sim.ts) |
| 20+ languages | CR-AS "EN + 20 More" | missing | English only (guess: no i18n found in src) |
| Optional permission pop-ups with a reason (notifications, camera) | CR-AS "Notice of Access Permission" | missing | none asked |

### Settings

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Help and Support inside the app | CR-AS "Settings > Help and Support" | missing | Settings has no help row (me.ts settings()) |
| Notifications on/off | CR-AS "Notifications" | missing | none |
| Privacy policy, terms, parent's guide linked | CR-AS | missing | none in Settings (grep privacy/terms) |
| Game Center achievements | CR-AS "This game also features achievements" | not-for-us | Daniel 2 Nov 07:3x, me.ts line 4: medals and counts "don't serve any purpose and are taking screen real state"; six achievements are coded and saved (store.ts ACHIEVEMENTS) but have no screen. His #50 "these are meant to be progressions" pulls the other way |

### Feedback and juice

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A result screen that celebrates (crowns, glory) | CR-SC | has | banner, ribbons, confetti (keeper/main.ts:454-456) |

### Monetisation

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Premium gems sold in packs | CR-AS Pouch/Bucket/Barrel of Gems | not-for-us | paid currency, nothing to sell at a booth |
| Monthly pass (Diamond Pass / Pass Royale) | CR-AS; CR-WP | not-for-us | paid pass |
| Special offers and random items | CR-AS "including random items" | not-for-us | paid loot |

## Clash of Clans


### Home screen

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Your own base is the home, alive and arrangeable | COC-AS "Customize your village" | partly | Pod home shows your lingzhi in its clearing (iphone-1-first.png); nothing to arrange |
| Producers fill up and you tap to collect | COC-WP "mines and storage buildings" | missing | none; the pod's readings are live but nothing accrues to collect |
| Builders and upgrade timers on screen | COC-WP "an unassigned builder is needed" | not-for-us | timers sold for gems; wrong for a booth |

### Core loop

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Attack another player's village with an army you assembled | COC-AS | partly | Walk duel: your three pets vs a neighbour's saved team (village/world.ts) |
| Defend with towers, traps, walls | COC-WP | partly | place Jar, Helper, Lamp around the lingzhi (sim.ts K.helpers) |
| Three-star rating for every battle | COC-WP "three-star scale" | missing | game-over shows waves and puffs only (keeper/main.ts:455) |
| Single-player campaign | COC-AS "Goblin King" | missing | none |
| Practice mode | COC-AS "Practice Mode" | missing | none |
| Replays and spectating | COC-AS "video replays" | missing | none |
| No waiting to play (training times removed 2025) | COC-WP "Clash Anytime ... removed training time" | has | the night starts at one tap (iphone-1-first.png) |

### Progression

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Town Hall levels that unlock buildings | COC-WP | missing | none |
| Research upgrades in a Laboratory | COC-WP | missing | none |
| Heroes unlocked at a level, with abilities | COC-WP "Hero Hall" | missing | none |
| More than one resource to juggle | COC-WP "Gold, Elixir, Dark Elixir, Gems" | partly | glow in the night (sim.ts), dew in Walk (world.ts); dew drew his anger, BUGS #29 |
| Ranked mode up to Legend League | COC-AS | missing | none |
| A second village (Builder Base) | COC-AS | missing | none |

### Collection

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Many troops, spells and heroes to mix | COC-WP (18 troops, 12 dark, 6 heroes) | partly | four duel pets (village/world.ts ALL) and three helpers |
| Hero skins and sceneries | COC-AS "Hero Skins and Sceneries" | partly | six lingzhi wearable on the Pod (me.ts) |
| Pets that assist heroes | COC-WP "Pet House" | missing | none |

### Rewards

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Loot from every attack | COC-AS "plunder loot" | partly | a Walk win gives the next lore card (world.ts) |
| Magic items from events and Clan Games | COC-WP | missing | none |

### Social

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Clans of up to 50 with troop donation | COC-WP | missing | none |
| Clan Wars and Clan War Leagues | COC-WP | missing | none |
| Clan Games (shared tasks) | COC-WP | missing | none |
| Clan Capital (shared base) | COC-WP | missing | none |
| Friendly Challenges against friends | COC-AS "Friendly Challenges" | partly | Walk duel vs a friend's saved team (village/world.ts); not live |
| Global chat | COC-WP "June 2026 ... Global Chat" | not-for-us | open chat needs moderation |

### Story and events

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Time-limited events | COC-WP "Magic Items ... through events" | missing | none |

### Onboarding

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A solo on-ramp that needs no other player | COC-WP "single-player campaign" | partly | guest play first, no account (shell.ts guest); the night is solo |

### Settings

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Help and Support, notifications, privacy and parent links | COC-AS | missing | none (see CR settings rows) |

### Feedback and juice

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Watch battles play out live | COC-AS "Watch Clanmates attack ... as a spectator" | missing | none |

### Monetisation

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Gems packs, Gold Pass, resource packs, special offers | COC-AS in-app purchase list | not-for-us | paid |

## Pokemon Sleep


### Home screen

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A home that tells you what happened while you were away | PS-AS "A New Day Dawns" | partly | "Since you were here Xh ago" line (app/home.ts sinceLine); not on the home itself |
| A centrepiece creature that grows with your care | PS-AS "Raise Snorlax big and strong" | has | lingzhi cap grows with the real pod (home.ts; iphone-4-pod-tap.png "49.9 mm") |

### Core loop

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Real-world sensor data drives the game | PS-WP "microphone and accelerometer" | has | pod humidity, warmth, CO2, light, water set growth and who comes at night (home.ts READ; sim.ts mix) |
| A daily rhythm: night, morning, afternoon | PS-OFF "A Day in Pokemon Sleep" | missing | no daily structure in app |
| Passive progress while you are away | PS-AS | partly | the lingzhi grows while the app is shut (pod server); no reward waits for you |
| Feed the centrepiece to grow it | PS-WP "give Snorlax berries and meals" | missing | none |
| Cook meals from collected ingredients | PS-G8 "Dishes and Recipes" | missing | none |
| Befriended creatures work for you | PS-WP "can be put on a team to collect berries" | missing | none |

### Progression

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A rank for the centrepiece that unlocks rarer visitors | PS-WP "rank will increase" | missing | none |
| A score after each session | PS-WP "Sleep Score" | partly | waves and puffs ribbon (keeper/main.ts:455), not a single score |
| Research areas to unlock | PS-G8 "Research Areas" | missing | none |
| Creature levels, natures, skills | PS-G8 "Natures, Skills, Specialties" | missing | none |
| Missions list | PS-G8 "Missions and Achievements" | missing | none |

### Collection

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A dex you try to complete | PS-AS "complete your Sleep Style Dex" | has | six slots with silhouettes on Me (iphone-3-me.png), eight cards in Walk |
| Each locked entry says how to earn it | PS-AS | has | "Black / 40 puffs" under each silhouette (iphone-3-me.png) |
| Befriend visitors with biscuits | PS-WP "PokéBiscuits" | missing | none |
| Rare variants (shinies) | PS-G8 "Share your Shinies" | missing | none |

### Rewards

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A reveal when you wake | PS-AS | partly | "New: X lingzhi" card at game over (keeper/main.ts:455), not on opening the app |

### Social

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Add friends | PS-G8 "add friends" | partly | iphone-2-friends.png (hard-coded neighbours plus signed-in households) |

### Story and events

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Recurring themed events (New Moon Day, Meal Prep Week) | PS-OFF news; PS-WP "holidays, lunar phases" | missing | none |
| A named guide who frames the world (Professor Neroli) | PS-WP | missing | no guide; lore is text (Shennong Bencao Jing on Me); BUGS #23 "there are no NPCs" |
| News feed | PS-OFF "News" | missing | none |

### Onboarding

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Meet the guide and the centrepiece first | PS-WP "given a Snorlax by Professor Neroli" | missing | hint line only ("Hold your light on a puff", keeper/main.ts:264) |
| Pairing a smartwatch or health data | PS-OFF devices; PS-AS | not-for-us | Hygeia reads a pod, not a body |

### Settings

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Smart alarm that wakes you in light sleep | PS-AS | not-for-us | Hygeia is not a sleep app |
| FAQ and help site | PS-OFF "Frequently Asked Questions" | missing | none |

### Feedback and juice

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A report with charts of what happened | PS-AS "Check Your Sleep Report" | partly | 24-hour line chart per reading (iphone-4-pod-tap.png), no overnight summary |
| Calm music and sound | PS-AS "Pokémon-inspired music" | missing | no audio in src (grep AudioContext/Audio found livefeed.ts only, the dev voice channel) |

### Monetisation

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Paid bundles and in-game purchases | PS-OFF "Bundle Vol. 19 Includes Biscuits"; PS-PLAY | not-for-us | paid |

## Finch


### Home screen

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A pet at the centre that you look after | FI-AS "Take care of your pet by taking care of yourself" | has | lingzhi at the centre (iphone-1-first.png) |
| Pet energy that starts the day | FI-AS "energize your pet to go exploring" | missing | none |
| Morning and evening check-in entry points | FI-AS "Start mornings ... End days" | missing | none |

### Core loop

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Looking after the real thing makes the pet thrive | FI-AS | has | readings inside the band grow the cap; "green: what your lingzhi likes" (iphone-4-pod-tap.png) |
| A one-minute daily task that grows the pet | FI-AS "quick self-care exercises" | partly | a three-minute night (sim.ts); no daily task |
| The pet returns from adventures with a story | FI-AS "back from adventures to share stories" | missing | none |
| Habit and goal tracker | FI-AS | not-for-us | Hygeia is a mushroom grower, not a habit tool |
| Journal, mood tracker, breathing, quizzes, quotes | FI-AS | not-for-us | wellness content, not Hygeia's job |
| Insights from your own data over time | FI-AS "Insights" | partly | 24-hour chart per reading (iphone-4-pod-tap.png); nothing over weeks |

### Progression

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| The pet grows through stages | FI-AS "grow your pet" | has | stage words and cap mm (home.ts stageWords) |
| Rewards earned from tasks to spend | FI-AS "earn rewards" | missing | no spendable currency |
| Streaks and wins you have accumulated | FI-AS "celebrate wins you've accumulated" | missing | none (grep streak) |

### Collection

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Seasonal collectible companions (Micropets) | FI-PLAY "Hidden Hollow, with new cozy Micropet" | missing | none |

### Rewards

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A celebration after you finish | FI-AS "celebrate wins" | has | confetti and ribbons (keeper/main.ts:395, 454) |

### Story and events

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Time-limited seasonal events | FI-PLAY "Events & offers: Ends on 11/29" | missing | none |

### Onboarding

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Exercises personalised for you | FI-AS "personalized for you" | missing | none |

### Settings

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Request deletion of your data in the app | FI-PLAY "You can request that data be deleted" | has | Me > Settings > Delete (/tmp/zhiverse-skeleton/4-delete.png) |
| Community and support links | FI-AS Discord, Instagram, support email | missing | none |

### Monetisation

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Subscription (Finch Plus) and Guardian Program | FI-AS in-app purchase list | not-for-us | paid subscription |

## Honkai Star Rail


### Home screen

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Your character and party in a 3D world | HSR-WP "out-of-combat gameplay" | not-for-us | open RPG exploration; a booth gets a clearing, not a world |
| Redeem codes | HSR-G8 "Version 4.7 Codes" | missing | none |
| Version banner with the new content | HSR-AS 4.6 release notes | missing | none |

### Core loop

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Turn-based combat with a team of four | HSR-WP | not-for-us | different genre; Hygeia is real-time |
| Weakness break and combat types | HSR-WP | not-for-us | tied to turn-based combat |
| Auto-battle and fast-forward | HSR-WP; coworker 00:16-00:21 "Auto-Pilot game ... start with the auto everything" | missing | none |
| Explore small self-contained areas with chests and puzzles | HSR-WP | partly | Walk the village (village/main.ts), no chests or puzzles |
| Endgame challenge modes | HSR-G8 "Endgame" | missing | none |
| Side modes (management, match-style mini-games) | HSR-AS | partly | one extra mode, Walk (modes.ts) |

### Progression

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Characters with different stats you tune | HSR-WP; coworker 00:31 "每个角色的 stats 是不同的" | missing | lingzhi differ in colour only (kinds.ts) |
| Equipment: Light Cones and Relics | HSR-WP | missing | none |
| Abilities you unlock (Traces) | HSR-WP | missing | none |
| Mission list | HSR-G8 "Missions" | missing | none |

### Collection

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Collect characters with a role each | HSR-WP "character class referred to as a Path" | partly | six lingzhi, no roles |
| Earn collectibles by challenge, not by paying | coworker 04:19-04:52 (Tiawei: "a specific challenge for a specific character") | has | each lingzhi earned by its own challenge, never bought (kinds.ts header) |
| Outfits | HSR-G8 "Cosmetics"; HSR-AS "New Outfits" | partly | wear a lingzhi on the Pod (me.ts) |
| A detail page for each character | HSR-WP | partly | tap a lingzhi on Me for its card (me.ts card()) |

### Rewards

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Free premium currency from play | HSR-WP "Stellar Jade ... earned through gameplay" | missing | no currency |
| A dramatic pull or reveal | HSR-WP "warping" | partly | "New: X lingzhi" card with confetti (keeper/main.ts:455) |

### Social

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Friends | HSR-AS "play with friends" | partly | iphone-2-friends.png |
| Chat | HSR-AS "Messaging and Chat" | not-for-us | moderation |

### Story and events

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A voiced main story told world by world | HSR-AS; HSR-WP | missing | text lore only |
| Voice-over in four languages | HSR-AS | missing | no audio |
| Companion characters with their own arcs | HSR-AS "Fateful Encounters" | missing | none (BUGS #23 "there are no NPCs") |
| A new version of events and story every cycle | HSR-AS 4.6; HSR-G8 4.7 | missing | none |
| Original score | HSR-AS "HOYO-MiX's original score" | missing | no audio |

### Onboarding

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Progress follows you across devices | HSR-WP "cross-save support" | partly | "Keep your lingzhi on any phone: Make an account" (iphone-3-me.png) |
| Several text and voice languages | HSR-AS | missing | English only (guess) |

### Settings

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| A way to reach customer service | HSR-AS "Customer Service Email" | missing | none |

### Monetisation

| Capability | Source | Hygeia | Evidence or why not |
| --- | --- | --- | --- |
| Shards sold in packs | HSR-AS Oneiric Shard list | not-for-us | paid currency |
| Monthly supply pass and battle pass | HSR-AS Express Supply Pass, Nameless Glory/Medal | not-for-us | paid |
| Paid random pulls for characters (gacha) | HSR-WP "warping"; HSR-AS "Contains Loot Boxes" | not-for-us | paid gacha; the earn-it version is the challenge row above |
