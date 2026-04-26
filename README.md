POLYSYNTH·1

8-voice polyphonic synthesizer in a single HTML file — built with Web Audio API. Zero dependencies.

Overview
POLYSYNTH-1 is a full analog-emulation polyphonic synthesizer that runs entirely in the browser. No frameworks, no npm install, no build step — just open the HTML file and play. It features a hardware-inspired UI with a complete signal chain: oscillators → filter → amplifier → effects.

Features
Oscillators

3 independent oscillators per voice — each switchable between Saw, Sine, Square, and Triangle waveforms
Per-oscillator tune, octave, and level controls
Oscillator sync and LFO-as-oscillator routing

Polyphony Modes
ModeVoicesPOLY 88 voicesPOLY 44 voicesDUOPH2 voicesMONO1 voice
Noise & Modulation

White and Pink noise generator with mix control
Glide/Portamento with adjustable time
LFO with multiple waveforms, routable to pitch, filter, or amplitude

Filter

State-variable filter — LPF, HPF, Notch modes
Adjustable Cutoff, Resonance, and Contour (env amount)
Dedicated Filter Envelope (ADSR)

Envelopes

Full ADSR (Attack, Decay, Sustain, Release) for both Amplitude and Filter

Effects Chain

Reverb
Delay
Distortion
Chorus

Arpeggiator & Step Sequencer

Built-in arpeggiator with multiple pattern modes
Step sequencer for programmable melodic patterns

Keyboard

On-screen piano keyboard with octave shifting ([ ] keys)
Full computer keyboard mapping for white and black keys
Shift = Sustain


Getting Started
No installation needed.
bash# Clone the repo
git clone https://github.com/yourusername/polysynth-1.git

# Open in browser
open polysynth-1.html
Or just download polysynth-1.html and double-click it.

Works best in Chrome or Edge. Safari and Firefox may have minor Web Audio API differences.


Keyboard Mapping
White keys:  A  S  D  F  G  H  J  K  L
Black keys:  W  E     T  Y  U     O  P

[  =  Octave Down
]  =  Octave Up
Shift  =  Sustain

How It Works
Everything runs on the Web Audio API — no external audio libraries. Each voice is an independent signal chain instantiated on note-on and released on note-off:
Oscillators (×3) ──┐
Noise Generator ───┼──► Mixer ──► Filter ──► Amp ──► Effects ──► Master Out
LFO ───────────────┘
The voice allocator handles polyphony by tracking active voices and stealing the oldest note when the voice limit is reached.

Tech Stack

Vanilla JavaScript — no frameworks
Web Audio API — all sound synthesis
HTML/CSS — single self-contained file


Screenshots

(Add your screenshot here)


License
MIT — use it, fork it, mangle it.

Author
Rudra Girdhar — B.Tech IT @ MAIT, Delhi
GitHub · Email
