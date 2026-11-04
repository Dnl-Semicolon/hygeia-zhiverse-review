# FEEDBACK: Hygeia ZhiVerse as a booth judge would meet it (4 Nov 2026)

How this was made: I read `README.md`, `MATRIX.md`, `Golden rules.md`, `Table stakes.md` and `CONFIRMED.md`, then opened every image with the Read tool: all 14 in `app-screens/` (iphone-1 to 6, ipad-1 to 6, `1-end`, `5-story`), all 14 in `art/` (s1–s6, red, white, yellow, blue, black, purple, nutrient, substrate) and all 3 in `references/`. Colours and contrast ratios below were sampled from the JPEG pixels (so they are ±a few units), and computed with the WCAG formula. I made no web searches; claims about how other games behave that are not visible in `references/` are marked **(from memory)**. Anything I inferred without seeing it is marked **guess**.

Out of scope as instructed: the reading console hidden behind the top bar on `iphone-1-first` / `iphone-5-play`, and the planned renames (tabs Home / Spirits / Rivals / Refills; readings Good / Low / High; a healthy pod makes your light stronger). Where I recommend something, I assume those changes have landed.

---

## 1. Ten seconds on the first screen (`iphone-1-first`, `ipad-1-first`), told nothing

**What I think it is:** "A mobile monster game whose background is a photo of some red, shiny mushrooms under purple light." I can't tell that it's a real mushroom in a real cabinet I would own. The camera is inside the box, so the cabinet (acrylic walls, fan, LED strips, water tray), which is the product, is never in frame. The one picture that shows it is `references/the-real-pod.jpg`, and the only app screen that shows it is the small photo on `iphone-4-pod-tap`, one tap deep. The word "HYGEIA" doesn't help: it names nothing I can see. Nothing says *lingzhi*, *grow*, *your pod* or *real*.

**What I would press:** DEFEND. It's the only gold thing on screen (`#FFCB56`, 12.8:1 against the `#130A1F` background) and it's huge. That is correct. But the button's icon is a **sword**, and the Rivals tab is **crossed swords**, while the game is *holding a light*. So I go in expecting to slash. The verb is wrong before I've played.

**What confuses me, in the order I'd notice it:**
1. **Three monsters standing still on the mushroom** (purple furball, horned orange ogre, green armoured thing). They aren't attacking or moving toward anything, and two are **cut off by the screen edge** (purple at left, green at right on `iphone-1-first`; same on `ipad-1-first`). It reads as a layout bug, not a threat.
2. **The top-left avatar is a cute mushroom girl, labelled "Sprout", over an empty grey bar.** By Jakob's Law, top-left avatar + name is *me*. But that face is Lin, the narrator in `5-story`. On Rivals, "You" is a different person (a red-hatted woman). So three pictures claim to be me. "Sprout" reads as a name, not a rank, and the bar has no fill, no number and no next step. The bar is `#433A4D` on `#130A1F`, **1.8:1**, so it barely exists.
3. **"CAM" pill top right with a dim dot.** The dot is `#5F2442` on `#281741`, **1.4:1**: is it recording or off? And what is CAM: switch camera? Live? At an offline booth, implying "live camera" is also a promise the booth can't keep.
4. **A thin gold line above DEFEND with nothing on it.** (This is the known console defect, but the judge sees it, so it's on the list of first-ten-seconds confusions.)
5. **A blue/indigo band peeks out between DEFEND and the tab bar** (`iphone-1-first`, y≈1550). It looks like a rendering seam.
6. **Four tabs: Pod, Shop, Rivals, Me.** The Pod icon is a "T in a box" I can't decode. Shop and Me are generic system icons (bag, person). That's a web-app tab bar, not a game hub.

**Verdict in ten seconds:** "cartoon tower defence on a mushroom photo." The two facts that make this product special are invisible: *it's your real pod at home*, and *the pod and the game feed each other*.

---

## 2. Screen by screen

The fix list is in §6; this section is the evidence.

### Global (every screen)
- **Text contrast is fine; component contrast is not.** Lilac body text `#C2B2D9` on a card `#241534` is 8.7:1. Tab icons `#A3A0A7` on `#0F0619` are 7.7:1. The failures are everything that shows *shape* or *state*. WCAG 1.4.11 asks for 3:1 on non-text UI:

  | Element | Sample | Ratio |
  |---|---|---|
  | Cards against the page (Rivals rows, Shop rows, reading chips) | `#241534` on `#130A1F` | **1.13** |
  | The dark bottom "lip" of every gold button | `#351400` on `#130A1F` | **1.15** |
  | Outline buttons "Done" and "Hear part 1 of the story" | `#392A49` on `#231433` | **1.31** |
  | CAM dot | `#5F2442` on `#281741` | **1.41** |
  | Rank / grow bars on home and Me | `#433A4D` on `#130A1F` (home), `#403641` on `#180B1F` (Me) | **1.8 / 1.65** |

  This is exactly the owner's "in dark mode you cannot rely on shadow alone." The gold buttons' depth comes from a dark shadow on a dark page, so it vanishes. Cards are tinted 1.13:1 off the page, so every list reads as a flat web table.
- **Four art styles that don't share a world:**
  - the photo/video of the pod;
  - glossy 3D clay creatures (`iphone-1-first`);
  - chibi stickers: Lin (`5-story`, top bar), the knight on the Helper button (`iphone-5-play`), and the flat clip-art mushrooms on the reward card (`1-end`);
  - painted Honor-of-Kings-grade heroes (`art/red, white, yellow, blue, black, purple`).

  On top of that, the story mixes Chinese ink-wash (`s1, s2, s3, s5`) with European oil painting (`s4, s6`).
- **One idea, many names:**
  - The action: DEFEND (home), "Guard your lingzhi" (`ipad-3-me`, Shop task), "Again" (end).
  - The enemies: creatures (brief), "puffs" (`1-end` "puffs gone"; Me challenge "40 puffs"), "sent away" (HUD).
  - The currencies: "glow" (fight), "+19" and "spores" (`1-end`), "points" (Shop).
  - The cap: "49.9 mm" (`iphone-4-pod-tap`) versus "5.0 cm" (`iphone-3-me`).
  - The helpers: "cards" (Me challenge "No cards") versus the Jar / Helper / Lamp buttons. No visible UI calls anything a card.

### Home: `iphone-1-first`, `ipad-1-first`
- Covered in §1. On iPad the layout is just the phone stretched: the top-bar name is ~11 pt, there is the same edge-clipping, and a large empty purple floor.
- **Hierarchy:** the only thing with weight is DEFEND. There's nothing about the player (rank, best, spirits owned), nothing about the pod (day, harvest, health), and nothing about tonight. MATRIX §2 #1 ("Where you stand, on the home screen") is still the top gap.

### Pod tap: `iphone-4-pod-tap` vs `ipad-4-pod-tap`
- **The same tap does two different things.** iPhone opens a readings page. iPad (`ipad-4-pod-tap`) stays on home and draws cyan airflow arrows from the fan. The iPad behaviour is the better idea (it's diegetic and matches `the-real-pod.jpg`), but it has no label. A judge sees arrows and doesn't learn "the fan just ran."
- The iPhone readings page is a **dashboard**: a big "88 %" ring, five identical chips, and a 24-hour chart. `CONFIRMED.md` says "no dashboard screen." It looks like a smart-home app, not a game.
- **The chips:**
  - The selected one is the only one with a state colour (green outline). The other four carry no good/bad signal (this is being fixed with Good/Low/High).
  - The layout is a 3+2 grid with an orphan row.
  - The chip card is 1.13:1 against the page.
- **The chart** "DAMP AIR, LAST 24 HOURS" is cut off by the tab bar and has no axis.
- **"Pod" stays highlighted in the tab bar** while you're on a pushed sub-page.
- **There is nothing to do here.** Shop's daily task says "Work the pod: mist, fan or light," but no screen I was shown has a mist, fan or light control. A judge who reads the task will look for them and not find them.
- **This page holds the best explainer in the app**, the wide photo of the cabinet, at a size and depth no judge will reach.

### Fight: `iphone-5-play`, `ipad-5-play`
- **Two circles, and I can't tell which is my light.** There's a large pale ring (`#D0D8CC`-ish) around the centre cap and a small white ring lower right. My guess: the big one is the lingzhi's zone and the small one is my finger. In a still frame the "light" has no glow, beam or warmth: it's a hairline. For a game whose whole fantasy is *holding light*, the light should be the brightest thing on screen. **(Guess: in motion there may be more; the still doesn't show it.)**
- **"♥ 100" floats on the top cap next to a monster.** Whose health is it: the mushroom's or that monster's? In the Clash Royale reference shots, HP bars sit *on* what they belong to and are coloured by side: blue for yours, red for theirs.
- **"0 sent away" with a lilac orb** is a score with no subject. Sent away *what*?
- **Bottom bar:** a green "2" glow meter, then right-aligned tiny text "glow: Jar 2 · Helper 4 · Lamp 4". A price list written as a sentence duplicates the cost badges already on the buttons. That's web-page thinking.
- **Helper and Lamp art:** Helper is a greyscale chibi knight and Lamp is a greyscale broom-like lamp. Greying out unaffordable items is correct, but the art is generic stock that matches neither the creatures nor the spirits. Meanwhile `art/yellow.jpg` is literally a hero *holding a glowing jar*, and `art/red.jpg` holds a *lantern staff*. The spirits already *are* Jar and Lamp, and the fight doesn't use them.
- **A pink/blue band shows under the helper row** (the video bleeding past the safe area).

### End of a night: `1-end`
- **The HUD and the card disagree:** the HUD says "Wave 2" while the card says "1 wave."
- **Stars:** 1 of 3 is filled, with no hint what earns the other two.
- **Numbers no one can read:** "+19" in orange next to "Sprout · +9 spores". Two different numbers, and a currency ("spores") that appears nowhere else. It also doesn't say what the bar under them is filling toward.
- **The spirit reveal uses the wrong image.** "New spirit: Red lingzhi — Ember Fighter" shows a flat clip-art mushroom, not `art/red.jpg`. The best art in the repo is the reward, and the reward screen hides it.
- **Two spirits at once in two small rows.** That dilutes the one "huh, nice" moment `CONFIRMED.md` Piece 5 asks for.
- **Confetti over the text:** it is drawn *above* the text, so "N w spiri . Red", "W ite", "lin zhi" are literally unreadable in the render.
- **Buttons:**
  - "Hear part 1 of the story" (the new, rare thing) is the weakest button, an outline at 1.31:1, while "Again" gets gold.
  - "Done" is also an outline, so the two secondary buttons look identical though one opens new content and one exits.
  - Nothing on this card says it moved me toward the RM5 refill reward.

### Story: `5-story`, `art/s1`–`s6`
- **The legend is a strong choice.** It's the White Snake: the snake becomes a woman (s1), meets Xu Xian at the bridge (s2), runs an herb shop with lingzhi on the wall (s3), the wine reveals her (s4), she takes the immortal lingzhi from its crane and deer guardians (s5), and revives him (s6). Lingzhi literally saves a life.
- **It's unconnected to the game.** The game's fantasy is *guarding a lingzhi*, and s5 *shows the guardians of a lingzhi*, but no line or image says "you are the guardian." The White spirit (`art/white.jpg`) has a white snake on her arm, so she is presumably Lady White, and that link isn't stated either.
- **s4 and s6 break the style:** European oil painting, a canopy bed, a wine glass, a Western-looking boy. They look like a different story. s6 also reads as romance more than revival, because he's already awake.
- **Lin's expression is a smirk/evil grin** (`5-story`, top-bar avatar) for a narrator about to tell a gentle legend.
- **The story only lives in a dialogue box,** which the owner already flagged ("people might skip over the dialogue"). The Skip button is at top right, and the text panel is the only carrier of meaning. With skip pressed, the art alone (snake on a mountain) explains nothing.

### Spirits / Me: `iphone-3-me`, `ipad-3-me`
- **It's a junk drawer:** a "You" hero (pod photo + "Sprout" + empty bar at 1.65:1 + cap size), a settings gear on top of the photo, Spirits with a three-line lore paragraph, the story strip, and a "Guard your lingzhi" button (iPad).
- **Locked spirits are greyscale "???" with a challenge label:**
  - "1 wave", "No cards", "3 waves", "Jars only", "40 puffs", "Till dawn".
  - "No cards" refers to a concept the UI never shows.
  - "1 wave" doesn't say *hold 1 wave* or *in one go*.
  - None says *what the spirit does for you*, so earning one has no stated payoff beyond owning it.
- **The story strip (`ipad-3-me`) is six empty dark boxes numbered 1–6.** There's no thumbnail, no lock icon, and no "earn the Red spirit to open." It looks like a broken image grid.
- **The lore paragraph** ("An old herbal, the Shennong Bencao Jing, sorts lingzhi into six colours…") is the only place the six-colour premise is explained, and it's a paragraph.

### Rivals: `iphone-2-friends`, `ipad-2-friends`
- **Five gold buttons on one screen** ("Play someone next to you" + four "Beat"). With everything primary, there's no primary.
- **"Play someone next to you":** I can't tell what it does. Two phones? Pass and play? Offline booth?
- **"Waves held in one go. Beat them to climb."** Climb to what? There's no reward for rank, and no link to the "Sprout" rank on home.
- **Avatar mismatch:** "Old Barnaby… oldest pod on the street" has the avatar of a young woman in purple. Wren, Pip and Juniper also use spirit-like painted portraits, so a viewer reasonably assumes rivals *are* spirits.
- **Hierarchy:** the bottom 45 % of the phone is empty. The flavour lines are charming ("Grew antlers by accident") but are the most visible text after the names.
- **Web table look:** cards at 1.13:1 and identical rows.

### Shop: `iphone-6-shop`, `ipad-6-shop`
- **The tab says "Shop", the page title says "Your pod".** (The rename to Refills fixes the tab, not the title.)
- **The reward card "RM5 off a nutrient cartridge, 0 / 60 points" is good.** It's the one place game ↔ refill is joined. But:
  - Points are earned only here: the end card shows spores, not points.
  - The three tasks are 10 each, so 30 a day. The 60 needs two days, which isn't stated.
  - The task rows look tappable, but nothing shows they lead anywhere.
- **The refill rows aren't tied to the pod.** "Substrate refill RM50" and "Nutrient cartridge RM30" have no buy button, no "add to order", and no *how much is left in my pod*. The readings page shows "Water 66 %". If that's the cartridge, it should say so here. **(Guess: I don't know whether Water = nutrient.)**
- **The art is fine:** the `nutrient.jpg` capsule and `substrate.jpg` box are clean product renders. But the capsule looks like a medicine pill, and nothing says it clips into the pod.

---

## 3. Connections a viewer will assume and not find

| The viewer assumes… | What the screens show | Evidence |
|---|---|---|
| **Pod → game.** If my pod is healthy, the game goes better. | Nothing in the fight mentions the pod. MATRIX says readings already decide *who comes at night* (`sim.ts mix`), which is a real link that's invisible on screen. The planned stronger light is not visible yet either. | `iphone-5-play`, MATRIX row "Real-world sensor data drives the game" |
| **Game → pod.** If I lose, does my real mushroom suffer? If I win, does it help? | Neither is answered. The creatures aren't named after anything real, so the fight reads as decoration on a photo. This is the owner's "the game doesn't do anything for the pod" in one line. | `iphone-1-first`, `iphone-5-play` |
| **Game → refills.** Playing earns me something toward refills. | The Shop says so, but the end card pays "spores" and "+19", not points, and doesn't mention the RM5 reward. | `1-end` vs `iphone-6-shop` |
| **Spirits → fight.** A spirit I earned fights with me. | Spirits only decorate (MATRIX: "the lingzhi you wear changes the Pod only"). Yellow holds a jar and Red holds a lantern, mirroring Jar and Lamp, but the fight uses a stock knight and broom. | `art/yellow.jpg`, `art/red.jpg`, `iphone-5-play` |
| **Story → anything.** Story parts unlock by playing, and the story explains why I guard. | Six empty boxes, and no stated unlock rule. The legend's guardians (s5) are never tied to the player. | `ipad-3-me`, `s5.jpg` |
| **Rank → Rivals.** Climbing Rivals raises my rank. | Two separate ladders: "Sprout" with an empty bar, and Rivals position 5. Neither says what's next. | `iphone-1-first`, `iphone-2-friends` |
| **Daily task "Work the pod" → a control.** | There is no mist/fan/light control on any screen shown. The iPad fan arrows appear on a tap, unlabeled. | `iphone-6-shop`, `ipad-4-pod-tap` |
| **The avatar top-left = me.** | It's Lin, the narrator. "You" on Rivals is someone else. | `iphone-1-first`, `5-story`, `iphone-2-friends` |
| **CAM = live view of my pod.** | It's unclear, and the booth is offline. | `iphone-1-first` |
| **Day 50 → harvest at some day.** | "Day 50" appears with no end. `CONFIRMED.md` says ~90 days, and the app never says so. | `iphone-4-pod-tap`, `iphone-3-me` |

---

## 4. What the reference games do for the same job

| Job | What the reference does (specific) | What Hygeia does |
|---|---|---|
| **Say what the game is in one glance** | Every Honor of Kings store frame (`honor-of-kings-appstore.jpg`) is a hero plus a **two-line caption**: a 2–4-word headline with a 5–8-word verb sub-line ("New Hero: Dunshan / Transform into a Turret, and fight as a tower"; "New Mode: Honor Royale / Super Fun Three-Minute Battle"). It's exposition without dialogue. | The home has a wordmark ("HYGEIA") and a button ("DEFEND"). No sub-line. |
| **Show whose thing is whose** | Clash Royale (`clash-royale-appstore.jpg`, all four arena shots): your towers and units are **blue**, the enemy's are **red**. HP bars sit on the unit and show a level badge. Colour = side, everywhere. | "♥ 100" floats between a cap and a monster. Ring colours (pale green, white) carry no side meaning. |
| **Make the arena the hero** | The Clash Royale frames are 100 % arena: the HUD is two thin strips (player name/clan top-left, timer top-right in the last frame). | The home is the arena too, which is good, but it's cropped so tight the *product* (the cabinet) is lost, and creatures are clipped at the edges. |
| **Make the reward the art** | The Honor of Kings frames give the hero splash half the frame; the reward *is* the painted character. **(From memory:** Clash Royale's card unlock is a full-screen card flip, one at a time.) | The spirit unlock shows clip-art mushrooms, two at once, under confetti (`1-end`). |
| **Buttons that look pressable on dark** | **(From memory:** Supercell buttons (Clash Royale / Clash of Clans): a thick dark outline around the whole button, a lighter top highlight band, a darker bottom lip in the button's *own hue* (not a black shadow), and white or dark text with a dark stroke. Colour carries role: yellow/gold = main, blue = secondary, green = confirm, red = danger.) | Gold buttons rely on a `#351400` shadow that is 1.15:1 against the page. Secondary buttons are 1.31:1 outlines. |
| **Teach the verb without words** | **(From memory:** Clash Royale's first match is a scripted battle where a pointing hand drags the one card you need; Plants vs. Zombies' first lawn gives you one seed packet and one lane.) | A text hint, "Hold your light on a puff" (MATRIX `keeper/main.ts:264`). |
| **Frame the world with a character, briefly** | Pokémon Sleep: Professor Neroli *hands you* Snorlax (MATRIX PS-WP). The character does one act, not a lecture. | Lin talks only in the story, in a box you skip. |
| **Tell you something changed today** | Honor of Kings frames lead with *what's new* ("Season Mode: Flow State"). Finch "Events… Ends on 11/29" (MATRIX). | The home shows the same scene every time. Nothing says "tonight". |
| **Real-world input visibly changes the game** | Pokémon Sleep: your sleep type decides *which* Pokémon appear, and the morning screen says so (MATRIX PS-WP "microphone and accelerometer"). | Readings already decide who comes (`sim.ts mix`), and the app never says so. |

---

## 5. What a pod owner wants that this does not offer

1. **"Is it OK right now?" in one glance on the home screen**, not one tap deep. With Good/Low/High this gets closer, but the home has no single verdict ("All good" / "Needs you").
2. **"What do I do about it?"** A Low or High reading should come with the action, and the action should be a button: Mist now, Fan now, Light on/off. The Shop task asks for it; no control exists on any screen shown.
3. **"When do I harvest?"** Day 50 of ~90, shown as a countdown, plus the moment of harvest itself as the biggest event in the app. Nothing shows it.
4. **"When do I need to buy a refill, and can I buy it here?"** Cartridge and substrate remaining in days, and an order button. The Shop lists prices only.
5. **"Show me it grew."** A week-over-week timelapse or "cap 3.1 → 5.0 cm since you started." There's a 24-hour chart; nothing longer (MATRIX: "nothing over weeks").
6. **"What happened while I was away?"** "Since you were here" exists in code (`home.ts sinceLine`) but not on the home (MATRIX).
7. **"Tell me if something goes wrong."** Notifications with a reason (MATRIX §2 #15). The emergency break-through promised in `CONFIRMED.md` ("a real emergency breaks through unmistakably") has no screen.
8. **"What do I do with the lingzhi after harvest?"** Slicing, tea, drying. The story is about lingzhi as medicine (s3, s6), but the owner of a real lingzhi gets no next step.
9. **"Help / what does this pod send?"** No help, privacy or support anywhere (MATRIX §2 #14).

---

## 6. The 12 changes: best first, highest booth impression per minute

These are the colour roles used throughout. They introduce the owner's third accent: gold acts, teal is the pod's light, coral is the enemy.

| Role | Fill | Light / highlight | Dark lip / rim | Text on it |
|---|---|---|---|---|
| **Gold = the one action on a screen** | `#FFC83D` | `#FFE89A` | `#C27A00` lip, `#3A2200` rim | `#2A1600` |
| **Teal = your pod and your light** (matches the airflow arrows in `the-real-pod.jpg`) | `#2FD6C4` | `#9FF5EA` | `#127F74` lip, `#06302C` rim | `#04201D` |
| **Coral = creatures, danger, damage** | `#FF5A5F` | — | `#8E1F27` | `#FFFFFF` |
| **Page** | `#130A1F` | — | — | — |
| **Card** (2 px border `#4A3566`, giving 3.2:1 vs page) | `#2A1A40` | — | — | — |

### 1. Put the game in the button, and the verb in the icon. **Under 15 minutes**
- **Icon:** replace the sword on DEFEND with a sun/lantern glyph (24 pt).
- **Button text:** two lines, centred.
  - Line 1: **DEFEND** (keep the size).
  - Line 2: **"Hold your light on the creatures"**, 15 pt semibold, `#5A3A00`.
- **Button height:** 72 → 84 pt.
- **States:**
  - Pressed: translateY 4 px and lip 6 → 2 px.
  - Disabled: never shown.
- **Rivals tab icon:** crossed swords → a podium or two-figure glyph.

### 2. Show the pod powering the light, every night. **Under an hour**
This is the visible face of the planned "healthy pod makes your light stronger", plus the existing `sim.ts mix`.
- **When:** tap DEFEND, then play a 1.6 s **"Tonight" card** before the first wave. It's a centred card on a 60 % `#000` scrim; tap anywhere to skip.
- **Row 1:** the five reading pips as icons, each coloured Good `#2FD6C4` / Low or High `#FF5A5F`.
- **Row 2:** one line, chosen by state:
  - all Good: **"Your pod is healthy: light +50%"**
  - otherwise, name the worst reading, e.g. **"Dry air tonight: more Dust Imps"**
- **Animation:** the Good pips fly into the light ring.
- **In the HUD:** add a teal pill left of the score: ☀ **+50%**, teal border `#2FD6C4` on `#06302C`.
- **Name each creature after the reading that summons it:**

  | Creature | Reading that summons it |
  |---|---|
  | Purple furball → **Mould Puff** | High damp |
  | Orange ogre → **Heat Brute** | High warmth |
  | Green armoured → **Stale-Air Grub** | High CO₂ |

  This answers "what does the game do for my pod": the fight is the pod's invisible work, made visible.

### 3. Make the spirit reveal use the spirit art, one at a time. **Under an hour**
- **Each new spirit gets its own full-screen beat** after "Well Guarded!", before the summary card.
- **Layout:**
  - Background `#130A1F`, with a 1.2 s radial burst in the spirit's colour behind the art:

    | Spirit | Burst colour |
    |---|---|
    | Red | `#E23B2E` |
    | White | `#F2E8D5` |
    | Yellow | `#F5B82E` |
    | Blue | `#2FD6C4` |
    | Black | `#6A4C8C` |
    | Purple | `#A04BE0` |

  - The full `art/<colour>.jpg` at 80 % of screen height. It enters greyscale at scale 0.9, then colour and scale 1.0 over 0.5 s.
  - Under it: **"RED LINGZHI"** in 28 pt heavy white, **"Ember Fighter"** in 17 pt `#FFC83D`, and the reason in 15 pt `#C2B2D9`: "The first one you guarded."
  - One gold button: **"Next"** (or **"Hear part 1 of the story"** on the last spirit).
- **Confetti:** behind the text layer (z-index below), never over it.
- **The summary card** then lists spirits as 48 pt round portrait crops, not clip-art.

### 4. One word per idea; pay the refill reward on the end card. **Under an hour** (strings are under 15 minutes; the end-card row is the rest)

| Idea | Use everywhere | Replaces |
|---|---|---|
| The action | **Defend** | "Guard your lingzhi" on Me and in the Shop task → "Defend your lingzhi" |
| Enemies | **creatures** (with the names from #2) | "puffs" |
| HUD score | **"0 driven off"** | "0 sent away" |
| Me challenges | **"Light only"** | "No cards" |
| | **"40 creatures"** | "40 puffs" |
| | **"Hold 1 wave"** / **"Hold 3 waves"** | "1 wave" / "3 waves" |
| | **"Jars only"** / **"Till dawn"** | (keep as is) |
| Currency | **points**, the Shop's word | "spores" and "+19" |
| Cap size | **cm**, one decimal (5.0 cm) | 49.9 mm |

- **End-card points row:** directly under the stars, a reward bar.
  - Left: the 40 pt nutrient capsule thumbnail.
  - Middle: **"+10 points · 10 / 60 to RM5 off a nutrient cartridge"**.
  - Bar: track `#3A2A52`, fill `#FFC83D`.
- **Stars:** add a caption under them in 13 pt `#C2B2D9`: **"★ hold 1 wave · ★★ 3 waves · ★★★ till dawn"**.
- **HUD:** at game over, the HUD wave counter must equal the card's figure.

### 5. Replace the top bar with *where I stand* and *where my pod stands*. **Under an hour**
- **Remove** the "HYGEIA" wordmark and the CAM pill.
- **Left: the rank badge.**
  - A 44 pt shield in `#FFC83D` with rim `#3A2200`, showing a number (rank tier 1).
  - Beside it, "Sprout" in 17 pt white, over a bar 120 × 8 pt: track `#3A2A52` with a 1 px `#4A3566` border, fill `#FFC83D`.
  - Under the bar, 12 pt `#C2B2D9`: **"40 / 100 to Shoot"**.
  - Tap opens Spirits.
- **Right: the harvest pill.**
  - Teal border `#2FD6C4` on `#06302C`, text **"Day 50 / 90 · harvest in 40 d"**, 15 pt `#9FF5EA`.
  - Tap opens the readings sheet.
- **Avatar:** the player's equipped spirit (round crop of `art/red.jpg` once earned; a plain shield before). Lin appears only in the story.

### 6. An establishing shot: show the cabinet, then dive in. **Under an hour**
- **On every cold start:** show the wide pod still (the photo already on `iphone-4-pod-tap`, or `the-real-pod.jpg` with its cyan airflow arrows) full-bleed for 1.2 s, then zoom it over 1.0 s (ease-in-out) into the cropped video home.
- **Caption during the wide shot,** HoK-style, bottom-centred on a `#000` 50 % band:
  - Line 1: **"Your lingzhi pod"**, 28 pt heavy white.
  - Line 2: **"Grows it for you. You guard it at night."**, 15 pt `#FFC83D`.
- **Skip:** a tap skips it.
- **Re-entry:** show it again whenever the app is idle > 60 s, which suits a booth where judges arrive mid-loop.
- **Fix creature placement:** home creatures sit ≥ 24 pt inside the safe area (no edge clipping), and walk slowly toward the cap (a loop, 0.3 pt/frame) so they read as a threat.

### 7. One game-grade button system, one gold per screen. **Under an hour**

| Button | Style | Size / type |
|---|---|---|
| **Primary (gold)** | Fill `#FFC83D`; inner top highlight 3 pt `#FFE89A`; bottom lip 6 pt `#C27A00`; 2 pt outer rim `#3A2200` all round; text `#2A1600` | 20 pt heavy, height 56 pt, radius 14 pt |
| **Secondary (teal)** | Same build in teal: `#2FD6C4` / `#9FF5EA` / `#127F74` / rim `#06302C`, text `#04201D` | — |
| **Tertiary** | Plain text `#C2B2D9` 17 pt, underline on press | — |

- **States, all buttons:**
  - Pressed: move down 4 pt, lip shrinks to 2 pt.
  - Disabled: fill `#3A2A52`, text `#7D6E96`, no lip.
- **Retire outline-only buttons.**
- **Apply the system screen by screen:**

  | Screen | Gold | Teal | Tertiary |
  |---|---|---|---|
  | `1-end` | "Again" | "Hear part 1 of the story" | "Done" |
  | Rivals | Only on the top action | "Beat" (36 pt tall) | — |

- **Cards** become `#2A1A40` with a 2 pt `#4A3566` border (3.2:1 vs page). That's the depth cue that doesn't rely on shadow.

### 8. Refills driven by the pod, with an order button. **Under an hour**
- **Page title** = tab name: **"Refills"**.
- **Each refill row:**
  - The product image (existing art).
  - Name 17 pt white.
  - Status line 15 pt, coloured: **"In your pod: 66 % · about 12 days left"**. Teal if > 14 days, `#FFC83D` if 7–14, coral `#FF5A5F` if < 7.
  - A teal **"Order · RM30"** button on the right (opens a confirmation sheet; offline at the booth, show "We'll remind you at your next connection").
  - **Assumption:** Water = nutrient cartridge. If it isn't, use the real cartridge level.
- **Order:** whichever refill runs out sooner goes first.
- **Today tasks:**
  - The whole row is tappable and routes to its screen: readings sheet / pod controls (#11) / the fight.
  - Add a trailing chevron `#7D6E96`.
  - The reward card says **"30 points a day · 2 days to RM5 off"**.

### 9. Put the spirit in the fight. **Under an hour** for art; **more** for powers
- **Replace the stock helper art:**
  - The **Jar** button uses a round crop of `art/yellow.jpg`'s jar arm.
  - The **Lamp** button uses `art/red.jpg`'s lantern staff.
  - The **Helper** knight becomes the player's equipped spirit (portrait crop) once earned. Before then, it's a locked silhouette with a 2 pt `#4A3566` ring and the caption "Earn a spirit".
- **The power** (more than an hour, but name it now so the cards can say it):

  | Spirit | Power |
  |---|---|
  | Red, "Ember" | Creatures burn 2× faster in your light |
  | White, "Mender" | Heals the lingzhi 10 ♥ per wave |
  | Yellow | Jars cost 1 |
  | Blue | Hits the farthest creature |
  | Black | Slows creatures 30 % |
  | Purple | Light ring 1.5× wider |

  Each Spirits card carries its one line.
- **Delete** the "glow: Jar 2 · Helper 4 · Lamp 4" text; the cost badges already say it.
- **Health:** move "♥ 100" onto a teal bar anchored under the centre cap (your side = teal, per Clash Royale's blue/red rule). Creatures get coral HP pips.

### 10. Spirits tab: say what each spirit gives and what each unlocks. **Under an hour**
- **Spirit grid:**
  - Keep the 3 × 2 grid of greyscale silhouettes.
  - Add under each: challenge (13 pt `#FFC83D`, the words from #4) and power (13 pt `#C2B2D9`, from #9).
  - Earned cards: full colour, a 2 pt border in the spirit's burst colour, and a teal **"Equip"** button.
- **Lore:** replace the paragraph with one line: **"Six lingzhi colours from the Shennong Bencao Jing. Each is a spirit you earn by defending."**
- **Story strip:**
  - Six 3:4 thumbnails from `s1`–`s6`.
  - Locked = blurred 12 px + dark 60 % overlay + lock glyph + 12 pt "Earn a spirit".
  - Unlocked = full art + "Part n".
  - One story part per spirit, stated.
- **The "You" header shrinks to a 72 pt strip.** The rank lives in the top bar now (#5).
- **Settings:** the gear moves out of the photo to the screen's top-right, 44 × 44 pt.

### 11. Pod controls on the readings sheet, played on the video. **Under an hour** if the fan-arrow effect in `ipad-4-pod-tap` is reusable (**guess**); otherwise **more**
- **Make the iPhone and iPad behave the same:** tapping the pod opens a bottom sheet over the home (not a pushed page), at 60 % height.
- **Sheet contents:**
  - The five readings as Good/Low/High chips (planned).
  - Three teal buttons in a row: **Mist**, **Fan**, **Light**, each icon + word, 64 pt square.
- **Pressing one** closes the sheet and plays its effect on the video for 3 s:

  | Button | Effect |
  |---|---|
  | Fan | The cyan arrows from `ipad-4-pod-tap` / `the-real-pod.jpg` |
  | Mist | White particle drift `#FFFFFF` at 40 % |
  | Light | LED strip flare `#C86BFF` |

  A teal toast then reads **"Fan ran for 30 s"**, and the Today task ticks.
- **Keep the 24-hour chart** (minus the clipping) under "More" in the sheet. It's for the owner, not the judge.

### 12. Cleanup pass the judges will notice. **Under an hour**
- Remove the blue/indigo band between DEFEND and the tab bar (`iphone-1-first`) and the pink/blue band under the fight's helper row (`iphone-5-play`): extend the video or page colour to the safe-area bottom.
- Rivals:
  - Give "Old Barnaby" an old man's portrait, or rename the row to fit its art.
  - Fill the empty lower half with **"Climb to #1 for the Purple spirit's frame"**, or cut the space.
  - Rename "Play someone next to you" to **"2 players, 1 phone"** if that is what it does.
- Story:
  - Swap Lin's grin for a neutral smile wherever she narrates.
  - Re-render `s4` and `s6` in the ink-wash style of `s1`/`s2`/`s3`/`s5` (**more**: art, list for later).
  - Add one Lin line on Part 5: **"The crane and the deer guarded this herb. Tonight, you do."** That is the bridge from story to fight.
- iPad: raise top-bar and tab-bar type to ≥ 13 pt, and cap the content width at 600 pt centred so it isn't a stretched phone.

---

**What not to touch:** the light-holding fight itself, its pacing, and the gold DEFEND as the single loudest thing on the home screen. Every change above adds meaning around the game rather than replacing it.
