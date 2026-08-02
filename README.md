# The Hill Abduction

A single-file, self-contained cinematic retelling of the Betty and Barney Hill
incident of 19–20 September 1961, rendered in real time with Three.js.

**Live:** https://alexgrama-dev.github.io/hill-abduction/

## What this is

Seven acts, driven by one master timeline locked to the narration:

| Act | Title | |
|---|---|---|
| I | The Road | U.S. Route 3 at night, one car |
| II | The Light That Climbed | the point of light below the Moon |
| III | Indian Head | the craft, the ports, the figures |
| IV | Missing Time | the road with everything else removed |
| V | The Eyes | the shape Barney drew under hypnosis |
| VI | The Star Map | Marjorie Fish's bead-and-thread model |
| VII | What Remains | the beacon, the marker, first light |

Everything is generated in code. No models, no textures, no image files:
ridged-simplex terrain, an L-system spruce forest, a superformula solid for the
eyes, a lathed hull, GLSL sky and fog, and a seeded PRNG so the world is
identical on every load.

## Narration

Voiced by **Bill** (ElevenLabs, `eleven_multilingual_v2`) — old, American,
weathered, because this is an elegy and two of the people in it died before it
was settled.

Act boundaries are not estimates. The read was rendered once through ElevenLabs'
`/with-timestamps` endpoint, and every cut point comes straight off the returned
character-level alignment.

The published copy ships the narration embedded and the API key blanked. The
source keeps the live-synthesis path, which falls back to the embedded read and
then to silent timed captions.

Audio drives the picture as well as the clock: broadband and low-band levels
from an `AnalyserNode` feed the sky haze, the craft's underlight, the eyes, the
motes, the star halos and the lens aberration.

## On the history

The story is told as it was told, and then as it was answered. Act VI ends with
Marjorie Fish withdrawing her own conclusion, after Hipparcos measured the real
distances and the pattern came apart. Act VII gives the last word to Jim
Macdonald's aircraft warning beacon on Cannon Mountain — which flashes in the
same red as the craft's fins in Act III, on purpose.

The marker in the closing shot is real: the New Hampshire Division of Historical
Resources placed it at the roadside in July 2011. Its lettering is rendered as
blank engraved rules rather than text, because putting words on it would put
words in the state's mouth.

## Running it

Open `index.html`. That is all — Three.js loads from a CDN and nothing else is
fetched. Sound on.
