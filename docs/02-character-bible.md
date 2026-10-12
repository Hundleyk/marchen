# 02 · Character bible: the hero

![Character sheet](concept/character_sheet.png)

## Identity

| | |
|---|---|
| **Name** | *Working name:* **Nix**, from the German *Nixe*, a water spirit of the Grimm tales. The sheet leaves the name blank. |
| **Pronouns** | they/them (per sheet) |
| **Age** | Ageless; reads as a young adult |
| **Species** | Tide-born: a spirit the sea shaped into a person so it could go ashore |
| **Role** | Story-mender, the one who carries stuck tales to their endings |
| **Motto** | *like the ocean, I am both soft and strong* |

## Appearance (from the sheet)

* **Head:** bald by nature, smooth dome. Large, calm grey-lavender eyes with a winged upper lash line; pale lavender brows; small soft mouth.
* **Ear fins:** coral-pink, fan-shaped, with darker red rays and a cream base. They sit where ears would be and sweep up and back. A small lower lobe sits beneath each.
* **Skin:** warm, luminous peach with a faint iridescent sheen. Clear **bubbles** cling to the skin, densest across the top and right side of the scalp, the right cheek, neck and shoulders, scattered down the arms and legs.
* **Neck:** faint pink gill lines on each side of the throat.
* **Outfit:** a navy sea-silk bandeau with a scallop shell at the centre; a short navy wrap at the hips; a long skirt of translucent kelp layers in navy, periwinkle, sea green and mist, open at the front and longest at the back; sheer kelp drapes hanging from the upper arms.
* **Jewellery:** gold chain necklace with pearls, a shell pendant and a sea-glass teardrop; pearl drop earrings under the fins; pearl strands across the torso and hips; shells at the belt; pearl anklets with small crystal drops; barefoot.
* **Palette:** blush pink · lilac · periwinkle · navy · sea green · sand gold.
* **Silhouette:** fins plus the flared, ragged skirt. It must read at distance and in shadow.

## Personality

* **Curious.** Everything on land is new. Nix picks things up, smells them, asks what they're for.
* **Unhurried.** Speaks and moves like water at rest. Rarely interrupts.
* **Formal with land customs,** slightly wrong in charming ways (bows to doors, thanks rain).
* **Warm but direct.** Kind does not mean quiet; Nix will say the true thing.
* **When angry, the sea is angry.** Rare, and the world reacts (waves rise, light cools).

## Backstory

Tales are how the land talks to the sea. When the coast's stories stopped finishing, the tide stopped knowing when to turn, and the sea began to grow restless. It shaped Nix from foam, shell and memory and sent them ashore to find out why. Nix doesn't remember being born; they remember the first wave that carried them, and the sound of a story stopping mid-sentence.

## Voice

* Short sentences. Images from the sea. Never sarcastic.
* Soft lines: questions, reassurances. Strong lines: statements, promises.

| Situation | Soft | Strong |
|---|---|---|
| Meeting a scared child | "You're shaking like a tidepool. May I sit?" | "Nothing is taking you anywhere. I'm here." |
| A stuck villager | "Tell me where your story stopped." | "Your story is going to end today." |
| An Unfinished creature | "Hush. Go back to the foam." | "Break." |

## Expressions

Six expressions from the sheet, used in dialogue portraits and in-world on the model's face.

| Expression | When it's used |
|---|---|
| Neutral | Default; idle; listening |
| Happy (eyes closed, open smile) | Beat restored, gift received, Breath refilled after a long dry stretch |
| Concerned | Someone is hurt or scared; Breath under 25% |
| Surprised | Thread discovered; tide changes unexpectedly |
| Sad | A tale's ending is bittersweet; failing a Soft approach |
| Angry | Strong stance under threat; the Unfinished erasing someone |

## How the look drives gameplay

| Sheet element | Mechanic |
|---|---|
| Bubbles on the skin | **Breath** (stamina). Bubbles pop as it's spent and re-form in seawater. |
| Ear fins | **Listen** (reveals threads); fins flare as a danger tell. |
| Fin and skin colour | Stance indicator: cooler in Soft, warmer coral in Strong. |
| Kelp skirt and drapes | Movement read: float upward in water, snap back on Surge. |
| Shells and pearls | Story rewards; each finished tale adds one to the necklace. |
| Expressions | Dialogue and in-world reactions. |

## 3D modelling brief

For whoever builds the in-game model (artist, contractor or an image-to-3D pass with cleanup):

* **Style:** stylised anime, soft forms, about 7.5 heads tall, slender.
* **Budget:** 30–45k triangles hero model; face at least 2k; bubbles as a separate mesh or decals so they can be hidden in groups.
* **Rig:** standard humanoid (Godot `SkeletonProfileHumanoid` compatible), A-pose. Extra bones: 2 per ear fin (flare), spring-bone chains for 8–12 kelp strips and the arm drapes.
* **Face:** texture-swap or blend-shape expressions for all six expressions above.
* **Materials:** skin with subtle iridescence; translucent kelp (alpha-scissor friendly); pearl and shell with a nacre sheen; sea-glass.
* **Bubble groups:** split into ~24 clusters, ordered so head clusters go last (low Breath stays readable).
* **Deliverables:** `.blend` source, `.glb` export, textures, turnaround renders.
