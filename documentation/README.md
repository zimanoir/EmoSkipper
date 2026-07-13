# pulseFlesh v2.0 documentation

## Overview

pulseFlesh v2.0 is developing from a cable-connected bio-interface into a wireless wearable bio-sequencer and bio-data source.

The current prototype is at the stage-testing phase. It reads heart activity through ECG, muscle activity, and physical impacts, then converts the signals into CV for analog synthesizers. Artistic testing created the need to reconfigure the project for wireless performance.

## v2.0 direction

The v2.0 system consists of two independent devices that can work without one another and communicate over Wi-Fi when paired.

### Device 1: wearable interface

The separately available wearable device contains ECG and piezo sensing, its own power, reusable metal connectors, an ESP32-D board, a DAC output providing a separate stable ground for the ECG module, and bio-data output. An application controls the wearable over Wi-Fi.

### Device 2: hardware sequencer

The second device is an independent hardware instrument. When paired with the wearable, it receives bio-data over Wi-Fi and converts it into sequences for synthesizers. It provides physical controls, sequence visualization, wired MIDI, and CV outputs.

It will be available in either of two formats:

- a compact standalone box with one encoder for unified adjustment;
- a Eurorack module for direct integration with synthesizers.

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
two independent pulseFlesh v2.0 devices
        ├──→ wearable: ECG + piezo + power + bio-data + Wi-Fi application
        │
        └──→ hardware sequencer: physical controls + visualization
                    ├──→ standalone box with one encoder
                    └──→ Eurorack module

when paired: wearable → bio-data over Wi-Fi → hardware sequencer
                                                ↓
                                        sequences → MIDI + CV
```

See the [development roadmap](roadmap.md) for the current sequence of work.
