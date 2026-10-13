# 08 · Roadmap

## Milestones

| # | Milestone | Goal | Done when |
|---|---|---|---|
| **M0** | Design | These docs agreed | Open questions below answered |
| **M1** | Swim and dive prototype | Feel | Capsule stand-in: walk, swim, dive, surface with whistle, Breath by depth, gather pickups |
| **M2** | Harbour greybox | Core loop | Pier, harbour, the Shelf and the Pearl Banks blocked out; one dive job; low/high tide; one dialogue with word highlights |
| **M3** | Vertical slice | Show it | Act 1 fully playable (45–60 min) with final hero model, barnacle growth, journal, the first festival light |
| **M4** | Content | The game | Acts 2–5, all islands, cast arcs, the council vote, festival progression |
| **M5** | Polish | Ship | Accessibility, performance, cultural review, Steam page |

## Godot project plan

**Engine:** Godot 4.x (Forward+), GDScript.

```
marchen/
  docs/                    design docs (this folder)
  game/                    Godot project root (project.godot)
    scenes/
      player/              player.tscn, camera_rig.tscn
      world/               brinehaven, the_shelf, pearl_banks, water.tscn
      ui/                  hud.tscn, journal.tscn, dialogue.tscn, title.tscn
    scripts/
      player/              movement.gd, swim.gd, breath.gd, barnacles.gd
      world/               tide_clock.gd, dive_job.gd, npc_schedule.gd
      ui/
    autoload/              game_state.gd (day, act, belonging, words, friendships), audio_bus.gd
    data/                  words, dive jobs, dialogue, letters (.tres or JSON)
    art/ audio/
```

### Key systems
| System | Notes |
|---|---|
| `swim.gd` | Switches player between land and water movement at the waterline; 3D swim with buoyancy |
| `breath.gd` | Drain by depth zone; refill on surfacing; triggers the whistle |
| `tide_clock.gd` | In-game time and two tides a day; raises/lowers the water plane and toggles tide-only areas |
| `dive_job.gd` | Resource: location, pickups, pay, rules (closed beds) |
| `barnacles.gd` | Reveals barnacle mesh groups when belonging milestones are reached |
| `npc_schedule.gd` | Per-NPC routines keyed by time and tide |
| Dialogue | Dialogic 2 or a small custom system; supports word highlights and vocabulary-gated choices |
| Water | Water plane shader with caustics underneath; underwater post-process (fog, tint, muffled audio bus) |
| Skirt and fins | `SpringBoneSimulator3D` chains |

## Risks

| Risk | Mitigation |
|---|---|
| Cultural sensitivity | Inspired-by, not copied; invented names and rites; research notes in doc 09; seek review from readers with relevant lived experience before launch |
| Swimming feel | Prototype swimming first (M1); it's most of the game |
| Hero model quality | Build from the v2 reference via a 3D artist or image-to-3D with cleanup; prototype with a capsule |
| Heavy themes overwhelm cozy | Every act balances tension with friendships, discoveries and quiet evenings |
| Scope (5 acts, 6 places) | Act 1 slice first; reuse dive jobs and NPC systems across islands |

## Open questions

1. **Her name.** Keep *Nix*, or something else?
2. **Why she left home.** Current default: her reef is dying and young merfolk are sent to find work. Keep, or change?
3. **Legs or tail?** Current default: legs on land and in water (as on the reference sheet). Or does she change form?
4. **The aunt.** Keep the missing-aunt thread as the personal mystery?
5. **Platforms.** PC only, or also Steam Deck / console?
