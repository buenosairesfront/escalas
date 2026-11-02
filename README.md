**English** · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [日本語](README.ja.md) · [中文](README.zh.md) · [हिन्दी](README.hi.md)

# U-MA Escalas

A piano scale lab: pick a root and any of **61 scales**, and the app shows you its notes and intervals, how to finger it with both hands, its arpeggios, the chords that live inside it, and lets you string those chords into a progression that plays with smooth voice leading.

**▶ Open the app:** https://buenosairesfront.github.io/escalas/

Nothing to install. The interface is in Spanish.

## How it works

The page is a technical sheet in five numbered sections, with a **monitor** at the top (a keyboard that lights up what is sounding, plus readouts for scale, note, degree and chord) and a **transport bar** fixed at the bottom.

### 01 · Scale
- **Root:** the 12 notes (black keys show both spellings, e.g. C♯ / D♭).
- **Family:** major and its modes, melodic minor, harmonic minor, harmonic major, pentatonics & blues, symmetric, bebop and world scales. Or type in **Search scale**. Each card shows the shape of the scale as 12 dots.
- **Summary:** the big name, every note spelled correctly with its degree (1, ♭3, ♯4…), a coloured bar of the steps between notes (S semitone, T tone, 1½ tone-and-a-half, 2T two tones), the **scale on the staff**, and a **clock** with its shape on the circle of 12 notes.

### 02 · Keyboard and fingering
The scale on a large keyboard with a coloured circle and finger number on each key (thumb, index, middle, ring, little), for the right hand, the left hand or both. Switch the view between **Keyboard** and **Staff**. Under it, a table with every note and its finger. Major and minor scales use the **traditional** fingering; for every other scale the app **calculates** one (it searches for the fingering with the fewest awkward stretches and thumbs on black keys) and labels it as such.

### 03 · Arpeggios
Pick the **degree**, the **type** (triad, with 7th, or quartal) and the **inversion**. You get the arpeggio over two octaves with its fingering, also traditional or calculated.

### 04 · Harmonisation
The scale **stacked** in triads or seventh chords: one card per degree with its roman numeral, name, quality (major, minor, diminished, augmented…), the chain of intervals, a mini keyboard, and its function (T tonic, SD subdominant, D dominant) when the scale is major or minor. Each card has **▶** to hear it and **+ PROG** to add it to the progression.

### 05 · Progression
Up to 16 chords, one 4/4 bar each. Load a preset (I–IV–V–I, ii–V–I, I–vi–IV–V, I–V–vi–IV, vi–IV–I–V, I–vi–ii–V, Andalusian cadence, circle of fifths, all the degrees) or build your own. The voices **move to the nearest inversion**, as a pianist would, and while it plays a large display shows the current chord and the bar.

### Transport (bottom bar)
- **What plays:** Scale, Arpeggio, Harmonised (the chords of the scale) or Progression.
- **▶ / ■** and **loop**, tempo, and metronome with beat lights.
- **Hands:** both, right (MD) or left (MI). **Direction:** ↑ or ↑↓. **Octaves:** 1 or 2.
- **Sound:** Piano, EP (electric piano) or Pad.

In the header you can switch note names (**Do Re Mi** or **C D E**) and light / dark theme. Everything you choose is remembered in the browser.

## Under the hood

A single `index.html` with no dependencies. Each scale is written as a formula of degrees (`1 2 ♭3 4 5 6 ♭7`), so every note is spelled with the right letter for the chosen root; chord names and roman numerals are worked out from the actual intervals. Calculated fingerings come from a dynamic-programming search over the five fingers of each hand. Drawings are `<canvas>` and SVG; the three sounds are synthesised live with Web Audio (no samples).

## Run locally

Download `index.html` and open it, or serve the folder:

```
python3 -m http.server 8000
```

<!-- u-ma:more -->
**More from U-MA:** every instrument and tool in one place → [U-MA showcase](https://github.com/buenosairesfront/U-ma)
<!-- /u-ma:more -->

## Credits

Traditional scale and arpeggio fingerings as taught in piano method books. App by U-MA サウンド · [Buenos Aires Front](https://www.instagram.com/buenos.aires.front/).
