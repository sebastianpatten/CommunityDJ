# The decks

The bottom half: two decks, each with a section map, a waveform, a spinning
disc, and its BPM and key. Everything that moves the music is on the
controller — the screen shows you what's happening.

## Stems

Sholto splits every track into four parts and groups them into three you can
play with: **drums**, **vocals**, and **instrumental** (bass and everything
else). Drop the vocal out, bring the beat back, all live.

**On screen:** the three chips under the disc — **DRMS** (blue), **VOX**
(green), **INST** (red). Filled in means you can hear that part; hollow with
coloured text means it's muted. The chips appear only once the stems are ready,
and they show state — they aren't buttons.

**Controller:** on the **HOT CUE** pad page, pads **1**, **2** and **3** on that
deck toggle drums, vocals and instrumental. The pad lights follow the chips.

Stems need **demucs** installed. The first analysis of a track takes roughly
half a minute to a few minutes; after that it's instant. The four files are
cached under `~/.local/share/sholto/stems/` and are uncompressed — budget around
250 MB a track. Beat loops need them too, so a very fresh track won't loop for
the first few seconds.

### Stem levels

**Controller:** hold the stem-level button and the three **EQ** knobs on both
decks stop being an EQ and become stem faders instead — **HI** rides the drums,
**MID** the vocals, **LOW** the instrumental. Let go and they're an EQ again.
This is a smooth ride, unlike the pads, which are a hard on/off.

## Play, pause and the brake

**Controller:** **PLAY/PAUSE**.
**Keyboard:** **P** for Deck 1, **Shift + P** for Deck 2.

Pausing doesn't cut the sound dead — the deck spins down like a turntable whose
motor was switched off, about half a second, then stops. Press again while it's
still slowing and it changes its mind and comes back up to speed. A deck won't
start until its beat detection has finished.

## The platter

**Touch the top and turn** and you're scratching; the sound follows your hand,
and a hand resting still holds the deck still. **Let go** and it resumes from
exactly where you left it — unless you *spun* it, in which case it coasts on
like a weighted platter and settles back into playback. A backspin dies out
about twice as fast as a forward fling.

**The side ring** is the fine one: small, precise nudges, no scratch sound.
**SHIFT + the platter top** is a silent fast search, about twice the normal jog
step.

While a loop is running the platter is ignored, so a scrub can't drag the
playhead out of the loop.

## CUE and headphones

| Control | What it does |
|---|---|
| **CUE** on the mixer (per deck) | Adds that deck to your headphones. The button lights while it's on |
| **MASTER CUE** | Adds the main mix to your headphones as well |
| **SHIFT + CUE** | Jumps the track back to the very start, still playing if it was playing |
| **CUE** on its own (the transport button under PLAY) | Nothing |

The headphone/master blend is the FLX-4's own **MIXING** knob.

## Loops

**Controller:** **4 BEAT / EXIT** starts a loop of four bars — one phrase —
snapped to the beat you're on. Press it again to come out. **½×** halves the
running loop, **2×** doubles it.

**On screen:** the loop shows on the waveform as a translucent band with bright
edges at the loop in and out points.

## Tempo

**Controller:** the tempo fader speeds the deck up or down. **SHIFT + BEAT
SYNC** cycles how far it reaches: **±6% → ±10% → ±16% → WIDE**. While the fader
is off centre, two small chips pop out above and below the BPM in the disc — the
original tempo on top, the current range underneath.

## Beatgrid

Sholto's beat detection is good but not perfect. Two things fix it.

**Correcting a doubled or halved tempo** — click the BPM in the middle of the
disc to open the tuner, then press **½**. That's the one-tap fix for a slow
track read at twice its speed. The correction sticks to that track.

**Sliding the grid onto the kicks** — from the tuner, or from the keyboard:

| Control | What it does |
|---|---|
| **G** | Open the tuner on the deck you're working on |
| **↑ / ↓** | BPM ±0.1 (**Shift** for ±1) |
| **← / →** | Slide the grid ±10 ms (**Shift** for ±1 beat) |
| **⟲** in the tuner | Back to what the analysis found |
| **×** or **Esc** | Close |

**Controller:** hold a deck's **SHIFT** and press the **← / →** arrow buttons to
shift that deck's grid a whole beat at a time — the quick fix when the downbeat
landed on the wrong beat of the bar. If a loop is running it moves with the
grid, so you can tap until the loop sits right by ear.

Once you've nudged a grid, the loop band on that deck's waveform turns **red**
— a reminder that this loop is on your grid, not the detected one.

Fix the spacing with **↑ / ↓** first, then line it up with **← / →**.

## EQ, filter and faders

- **EQ HI / MID / LOW** — a three-band isolator per deck. All the way down is
  silence, not just quiet.
- **FILTER** knob — centre is off, left sweeps a low-pass down, right sweeps a
  high-pass up.
- **Channel fader** — that deck's level. The waveform draws a thin horizontal
  line at the fader's height so you can see it.
- **Crossfader** — the blend between the two decks.

When a deck ends up completely silent — fader down, or the crossfader all the
way to the other side — the whole deck panel washes red.

## Echo

**Controller:** switch the pads to **PAD FX1** and press pad **1**. It's a
half-beat echo locked to the track's tempo. Switching it off stops feeding it
but lets the tail ring out — the classic echo-out, rather than a dead cut.

## Markers

**Keyboard:** **M** drops a marker on Deck 1 at the spot it's playing,
**Shift + M** on Deck 2. A short confirmation appears at the bottom of the
window, and the marker shows on the waveform as a hot-pink line with a flag on
top. Markers are saved with the track.

## Magnetic beat-snap

When both decks are playing, both analysed, and their tempos are within about
half a percent, a green chain-link icon appears between the two discs: the
magnet is available. Nudge a deck with the jog wheel and, as the beats come
close, both waveforms glow green on the beat and the wheel gently holds. Let go
and that deck locks to the other one's grid, tempo included. Nothing to arm — it
just happens. While you're turning the wheel the glow becomes a full-height
green line on both decks, so you can see the two line up.

## Section map

The thin strip above each waveform is the whole song at a glance: one block per
section, labelled **INTRO**, **BUILD**, **DROP**, **BREAK**, **VERSE**,
**CHORUS**, **BRIDGE**, **OUTRO**. Calm sections are see-through, intense ones
full colour, and a line marks where you are. The colours come from your theme.
It is display-only — clicking it does nothing; use the platter or **SHIFT +
CUE** to move.

## Waveform

The big scrolling view. The playhead is the vertical line down the middle; the
track moves under it.

| What you see | What it means |
|---|---|
| Blue outer shape | Bass |
| Orange middle | Mids |
| White core | Highs and transients |
| Full-height vertical lines | Downbeats — the 1 of each bar |
| Small ticks along the top | The other beats |
| Thin green bars in the middle | Where the vocals are. They grey out when VOX is muted |
| Translucent band with bright edges | The active loop (red if you've nudged the grid) |
| Hot-pink line with a flag | A marker you dropped |
| Thin horizontal line | The channel fader's level |
| Green glow on a beat | Magnetic beat-snap |

Height is loudness, so a quiet intro reads short and the drop reads tall. Move
the tempo fader and the waveform squeezes or stretches to match.

## Disc and BPM ring

The disc turns once per bar, in time with the track. Its outer ring is your
progress: **green** at the start, through yellow and orange, to **red** at the
end, flashing over the last tenth — the deck's **BEAT SYNC** light on the
controller flashes with it. The number in the middle is the live BPM; click it
to open the tempo and beatgrid tuner.

## Key chip and Camelot

Under the title is the track's key as a Camelot code — **8A**, **12B** and so
on. Same number, same key; one step around the wheel, or the same number with
the other letter, and it will mix harmonically. The chip's colour matches that
key in the library list, and the library outlines every chip that mixes with
what's on the decks.
