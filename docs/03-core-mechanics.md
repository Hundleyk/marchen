# 03 · Core mechanics

All numbers are starting values for prototyping, meant to be tuned.

## Core loop

```
Arrive in a district (tide stuck)
  → Listen: find loose threads (stuck story beats)
  → Explore at different tide levels, Soft or Strong
  → Restore each beat (puzzle / dialogue / soothe or scatter the Unfinished)
  → All beats done → tale ending plays → shell on necklace, ability upgrade
  → Tide in that district starts turning on its own → next district
```

Moment to moment: **move → spend Breath → find water → refill → move.**

## 1. Soft and Strong (stance)

Tap **Q** to switch. Switching is instant, costs nothing and has a 0.4 s cooldown. Fins, skin sheen and kelp tint shift (cool lilac for Soft, warm coral for Strong).

| | **Soft** (ebb) | **Strong** (flood) |
|---|---|---|
| Ground speed | 4.5 m/s walk, 6.0 run | 4.0 walk, 8.0 sprint |
| Jump | Float-jump 2.4 m; hold to hang 0.6 s | Heavy jump 1.6 m; ground slam on landing |
| Air | **Glide** (hold Shift): fall 1.2 m/s, 7 m/s forward | **Surge** (Shift): 6 m dash, 0.25 s, breaks brittle walls |
| Swim | 7 m/s, can ride currents | 5 m/s, can swim *against* currents |
| Tide stones | **Lower** the tide one level | **Raise** the tide one level |
| Water action | Calm a whirlpool or current | **Wave push** (LMB): shove objects 4 m |
| People | Comfort / coax / listen dialogue options | Insist / protect / confront dialogue options |
| The Unfinished | **Soothe** (hold E near one, 2 s): returns it to foam permanently | **Scatter** (Surge or wave push): gone instantly, re-forms after 60 s |

**Design rule:** every stuck beat must be solvable in either stance. Soft routes are usually slower and safer; Strong routes are faster and messier. Each route gives a different small reward (a dialogue memory vs. a found item).

## 2. Breath (the bubble meter)

Breath lives on the hero's body as **24 bubble clusters**. There is no on-screen bar.

| Action | Cost |
|---|---|
| Glide | 1 cluster per 1.5 s |
| Surge | 4 clusters |
| Float-jump hang | 1 cluster |
| Wave push | 3 clusters |
| Listen | 1 cluster per 2 s held |
| Soothe | 2 clusters |
| Hit by an Unfinished | lose 3 clusters, knocked back 3 m |

| Source | Regen |
|---|---|
| Standing or swimming in **seawater** | 6 clusters/s |
| Rain | 1 cluster per 2 s |
| Sea-spray zones (rocks, piers) | 1 cluster/s |
| Fresh water (wells, rivers) | none, and it's flagged in Nix's dialogue |

* Clusters pop in a fixed order: legs → arms → shoulders → head. The last 6 clusters are on the head, so low Breath is always readable.
* **At 0 Breath** Nix can walk, swim slowly, talk and use tide stones, but no abilities. No death from Breath.
* Max Breath grows to 32 via shells (see Progression).

## 3. The tide

Each district has **three tide levels** and 1–3 **tide stones**.

| Level | Water height | What opens |
|---|---|---|
| **Ebb** (low) | −1.5 m | Tidepools, sea caves, sunken streets, the seabed |
| **Slack** (mid) | 0 m (default on arrival) | Normal town, piers usable |
| **Flood** (high) | +2.0 m | Rooftop islands, boats float free, swim routes link areas |

* Using a stone in Soft lowers one level; in Strong raises one level. 3 s transition with a visible wave front.
* Tide level persists per district. After a district's tale is finished, its tide **cycles on its own** (3 minutes per level) unless the player uses a stone.
* NPCs and objects react: boats rise, crabs scuttle into the open at Ebb, gulls perch on high roofs at Flood.

**Puzzle verbs the tide enables:** float an object up to a ledge; strand an object on the seabed; open or seal a cave; create a swim route; reveal or drown a path.

## 4. Listen and threads

* Hold **F**: world desaturates, ambient music drops to the district's tide song, Nix's fins flare.
* **Loose threads** glow within 25 m: the objects at the heart of a stuck beat (a dropped comb, an unsent letter, a half-sewn shirt).
* Interacting with a thread starts that beat and adds it to the journal.
* Listen also reveals **currents** (swim routes) and **brittle walls** (Surge targets).

## 5. Story beats

A beat is a small objective tied to one moment of the tale. Each district has 3–5 beats.

**Beat template:**
1. **Thread:** the stuck object or person.
2. **Obstacle:** something the tide, a stance ability or a dialogue choice resolves.
3. **Two routes:** a Soft solution and a Strong solution.
4. **Restoration:** a 5–10 s in-world vignette where the frozen moment completes.

Example (Nixmill): *The Thrown Comb*. The fleeing sister's comb hangs in the air over a channel, frozen. Soft: lower the tide, walk the seabed and float-jump up to catch it. Strong: raise the tide, swim against the current and wave-push the comb free.

Glide and wave push are unlocked by shells (see Progression); beats that come before an unlock either avoid that ability or lend it for that beat only.

## 6. The Unfinished

Creatures of torn pages and sea-foam that gather where stories stall. They never kill; they **erase** (knock Breath off, push Nix back) and block paths.

| Type | Behaviour | Soft answer | Strong answer |
|---|---|---|---|
| **Foamling** | Drifts toward Nix, slow | Soothe (2 s) | One Surge or push |
| **Page-gull** | Swoops from above, steals a thread item | Calm by standing still in Listen | Wave push it out of the air |
| **Inkwell** | Stationary pool that spreads at Ebb, shrinks at Flood | Lower tide and soothe its core | Raise tide to drown it |
| **The Stopped** (district guardian) | A huge half-written figure; patterned attacks | Complete its sentence via dialogue under pressure | Break its pages with Surge between patterns |

## 7. Progression

* **Shells** (one per finished tale) go on the necklace and unlock or upgrade abilities:

| Tale | Shell | Unlock |
|---|---|---|
| Nixmill | Comb shell | Glide |
| Fisher's Hollow | Storm pearl | Wave push |
| Swanreach | Feather shell | Float-jump hang +0.6 s |
| Undine's Rest | Well crystal | Listen range 25 → 45 m; see threads through walls |
| The Glass Deep | Final shell | The tide turns everywhere (ending) |

* **Pearls** (side collectibles, ~10 per district): every 5 pearls = +2 max Breath (cap 32).
* **Tale memories** (from Soft routes) and **found keepsakes** (from Strong routes) fill the journal and unlock home decorations.

## 8. Failure and checkpoints

* No deaths. Falling into deep water outside the play area washes Nix back to the last tide stone.
* The Stopped can "erase" Nix fully (0 Breath + hit): fade to foam, restart the encounter phase with full Breath.
