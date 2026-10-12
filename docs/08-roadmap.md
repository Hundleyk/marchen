# 08 · Roadmap

## Milestones

| # | Milestone | Goal | Done when |
|---|---|---|---|
| **M0** | Design | These docs agreed | Open questions below answered |
| **M1** | Movement prototype | Feel | Capsule stand-in with WASD, camera, float-jump, Glide, Surge, Soft/Strong switch, Breath (as 24 spheres on the capsule), seawater refill |
| **M2** | Tide prototype | Core puzzle | Greybox Landing Beach + Tidepools with one tide stone and 3 water levels, one Foamling, one thread with Listen |
| **M3** | Vertical slice | Show it | Nixmill fully playable (20–30 min) with final hero model, dialogue, expressions, tale ending |
| **M4** | Content | The game | Districts 2–5, the Stopped encounters, music layers, journal |
| **M5** | Polish | Ship | Accessibility pass, performance, Steam page |

M1 and M2 cover "UI and core mechanics first": a single cove with one tide stone and one stuck beat is enough to test whether the pillars are fun.

## Godot project plan

**Engine:** Godot 4.x (Forward+), GDScript.

```
marchen/
  docs/                    design docs (this folder)
  game/                    Godot project root (project.godot)
    scenes/
      player/              player.tscn, camera_rig.tscn
      world/               districts, tide_water.tscn, tide_stone.tscn
      creatures/           foamling.tscn, page_gull.tscn, inkwell.tscn
      ui/                  hud.tscn, journal.tscn, dialogue.tscn, title.tscn
    scripts/
      player/              player_controller.gd, stance.gd, breath.gd
      world/               tide_manager.gd, thread.gd, beat.gd
      ui/
    autoload/              game_state.gd (tide per district, beats, pearls), audio_bus.gd
    art/ audio/ data/      data/ holds beats and dialogue as .tres or JSON
```

### Key systems
| System | Notes |
|---|---|
| `stance.gd` | Enum SOFT/STRONG; emits `stance_changed`; other systems read it |
| `breath.gd` | Int 0–24/32; `spend(n)`, `refill_rate`; emits `breath_changed` to drive bubble visibility |
| `tide_manager.gd` | Per-district level (-1/0/+1); tweens a water plane and toggles collision layers per level |
| Water | One `MeshInstance3D` plane per district + `Area3D` for "in seawater" detection |
| `beat.gd` | Resource: thread node, soft/strong completion flags, restoration animation |
| Dialogue | Small custom system or Dialogic 2; choice tags `soft` / `strong` |
| Kelp skirt | `SpringBoneSimulator3D` chains |

## Risks

| Risk | Mitigation |
|---|---|
| Hero model quality | Commission or image-to-3D + cleanup; prototype with a capsule until M3 |
| Tide changes break collision/navigation | Build each district with explicit per-level collision layers; test all 3 levels per beat |
| Two routes per beat doubles content | Keep beats small; reuse puzzle verbs; one Strong and one Soft route only |
| Diegetic Breath unreadable | Bubble ring at screen edge below 25%; optional bar in Accessibility |

## Open questions

1. **Hero name.** Keep *Nix*, or something else?
2. **The café.** Should there be a seaside café (on the Nixmill breakwater, or in Perlgrund) that doubles as Nix's base between districts (serving villagers whose tales you've finished)?
3. **Combat.** Keep the Unfinished as avoidance plus Soothe/Scatter, or add a light combo for Strong?
4. **Platforms.** PC only, or also Steam Deck / mobile?
5. **Tone of the finale.** Are both endings equal, or is there a hidden third ending for a fully balanced Soft/Strong playthrough?
