# Ear Training

Two browser-based ear trainers. Each is a single self-contained HTML file — no build step, no dependencies, no audio assets, no server. All sound is synthesized live with the Web Audio API.

**Live site:** https://USERNAME.github.io/ear-training/

---

## Key Sense — Functional Ear Trainer

Hear every note and chord *relative to the key*. A cadence establishes the tonic, then you answer.

| Mode | What it drills |
|---|---|
| **Degrees** | Scale degree recognition. Sing the note, walk it to `do`, commit out loud, then answer. A Resolve button plays the walk to the tonic. |
| **Chords** | Chord function ID in two-hand piano voicings. Home (tonic), moving away (subdominant), or pulling home (dominant) — then the numeral. At L5 the bass may play the 3rd or 5th, so the root crutch is gone. |
| **Progressions** | Progressions generated fresh from functional-harmony rules rather than drawn from a fixed list, so you can't pattern-match. From L3 up, chords appear in close, drop-2, drop-3, and drop-4 spreads. L5 adds inversions. |
| **Melody** | Short phrases sung back on degree numbers, then entered in order. |
| **Stats** | Degree and chord accuracy, plus your top confusion pairs to bias the next session. |

Five difficulty levels, key selection (or random), three instrument voices (piano, organ, strings), auto-next, and a built-in 50-minute session plan.

## Ben Monder Call & Response

The app plays a note. You play it back on your instrument within the beat. Right answer, new note. Wrong answer, the same note returns — and the note name stays hidden until you nail it.

Adjustable tempo, three tones (clean synth, plucked guitar, piano), three mic sensitivity settings, optional metronome click, and an optional exact-octave requirement. Tracks streak, best streak, accuracy, and per-tier first-try rate.

**Use headphones.** Otherwise the mic hears the app's own note and scores it as yours.

Pitch detection is pitch-class only by default — a guitar's written C sounds an octave lower than concert C, so exact-octave mode stays off unless you turn it on. Play one clean note per beat and let it ring.

---

## Running it

**Hosted:** just open the live site above. This is the recommended way to use Call & Response — microphone access requires a secure (HTTPS) origin, and Chrome blocks it for files opened directly from disk.

**Locally:** download the repo and double-click `index.html`. Key Sense works fine this way. Call & Response may not get mic permission depending on your browser; if so, serve the folder over localhost instead:

```
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Privacy

No accounts, no analytics, no network requests of any kind. The microphone stream in Call & Response is analyzed in the browser and never recorded, stored, or transmitted.

## License

MIT — see [LICENSE](LICENSE). Use them, fork them, adapt them for your own students.
