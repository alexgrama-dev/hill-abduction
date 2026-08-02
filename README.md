# The Hill Abduction

A single-file, self-contained cinematic retelling of the Betty and Barney Hill
incident of 19–20 September 1961, rendered in real time with Three.js.

**Live:** https://alexgrama-dev.github.io/hill-abduction/

## The seven acts

| Act | Title | |
|---|---|---|
| I | The Road | U.S. Route 3 at night, one car |
| II | The Light That Climbed | the point of light, and the binoculars |
| III | Indian Head | the craft, the ports, the crew, the run |
| IV | The Beeping | the road with everything else removed |
| V | What They Remembered | the roadblock, the trees, the table, the map |
| VI | The Star Map | Marjorie Fish's model, and its collapse |
| VII | What Remains | Simon's verdict, the beacon, the marker |

Twenty-three shots with hard cuts, driven by one master timeline locked to the
narration.

## Everything is generated in code

No models, no textures, no image files. Ridged-simplex terrain with a
corridor-flattened road; an L-system spruce forest; a lathed hull; Gielis
superformula solids for the eyes — used at full size in Act V and shrunk onto the
faces of the crew, so the shape Barney drew in 1964 is literally the same object
in both places; GLSL sky, fog and glow; and a seeded PRNG throughout, so the
world is identical on every load.

## Narration

Voiced by **Brian** (ElevenLabs, `eleven_multilingual_v2`) — deep, American, read
flat and unhurried. Stability is raised and style dropped on purpose: a level
voice stating what happened is more ominous than one acting it out, and the
terror in this account is in the facts.

Act boundaries are not estimates. The read was rendered once through ElevenLabs'
`/with-timestamps` endpoint, and every cut point comes off the returned
character-level alignment.

The published copy ships the narration embedded with the API key blanked. The
source keeps the live-synthesis path, which falls back to the embedded read and
then to silent timed captions.

## Sound

Synthesised in Web Audio from oscillators and one seeded noise buffer — wind
through the Notch, a 1957 straight-six that dies when they pull over, a 31 Hz
pressure under the craft, a heartbeat under the hypnosis, and **the beeping**,
which is the hinge of the whole account and which an earlier cut played over
silence.

Audio drives the picture as well as the clock: broadband and low-band levels from
an `AnalyserNode` feed the sky haze, the craft's underlight, the eyes, the motes,
the star halos and the lens aberration.

## On the history

The story is told as it was told, and then as it was answered.

Act V is the abduction as *hypnosis produced it* in 1964 — which is the only way
it exists. Act VI ends with Marjorie Fish withdrawing her own conclusion after
Hipparcos measured the real distances. The lattice in that act is built as a
plane plus depth, so it resolves into Betty's map from exactly one viewpoint and
from nowhere else, which is precisely what Fish claimed and what Sagan disputed.

Act VII gives the last word to the other side: Benjamin Simon, who recovered the
memories and did not believe them; the *Outer Limits* broadcast twelve days
before Barney drew those eyes; and Jim Macdonald's aircraft warning beacon on
Cannon Mountain, which flashes here in the same red as the craft's fins in Act
III, on purpose.

The marker in the closing shot is real — the New Hampshire Division of Historical
Resources placed it at the roadside in July 2011. Its lettering is rendered as
blank engraved rules rather than text, because putting words on it would put
words in the state's mouth.

## Controls

Pause/play (or **space**, or click the scene), mute, replay. Pause holds the
whole world, not just the voice: the shader clock stops with it.

## Running it

Open `index.html`. Three.js loads from a CDN and nothing else is fetched.
Sound on.
