# pulseFlesh v2.0 documentation

## Overview

pulseFlesh v2.0 is developing from a cable-connected bio-interface into a wireless wearable bio-sequencer and bio-data source.

The current prototype is at the stage-testing phase. It reads heart activity through ECG, muscle activity, and physical impacts, then converts the signals into CV for analog synthesizers. Artistic testing created the need to reconfigure the project for wireless performance.

## v2.0 direction

The core of v2.0 will be a separately available wearable interface with reusable metal connectors, an ESP32-D board, a DAC output providing a separate stable ground for the ECG module, Wi-Fi MIDI, and access to an application.

The wearable will work independently as a complete wireless bio-sequencer and bio-data source. Two optional hardware interfaces will extend it:

- a standalone box with wired MIDI, CV outputs, and one encoder for unified adjustment;
- a Eurorack module with MIDI and CV outputs for synthesizers.

## Current stage prototype

The existing prototype mixes ECG, muscle activity, and a piezo impact signal. It provides three CV outputs for synthesizer modulation and is currently used for stage testing.

Most connectors and parts in the current prototype were salvaged from broken electronics. The firmware filters short signal glitches, derives a chaos index from rapid signal changes, and applies a quadratic curve to emphasize heartbeats and muscle spikes.

## Project path

```text
current CV prototype
        ↓
stage testing
        ↓
artistic redevelopment
        ↓
wearable pulseFlesh v2.0 over Wi-Fi MIDI
        ├──→ application / receiving software
        ├──→ standalone MIDI + CV box with one encoder
        └──→ Eurorack MIDI + CV module
```

See the [development roadmap](roadmap.md) for the current sequence of work.
