# pulseFlesh v2.0 development roadmap

## Current phase: stage testing

The existing prototype is being tested in a stage context. This phase is used to understand how ECG, heart rhythm, muscle activity, impacts, and CV control behave as artistic material during performance.

The stage-testing process created the artistic need to reconfigure pulseFlesh as a wireless bio-sequencer and bio-data source.

## Phase 1: wearable interface

- Develop the wearable pulseFlesh v2.0 unit around ESP32-D.
- Use reusable metal connectors.
- Integrate ECG and piezo sensing.
- Provide the wearable with its own power.
- Use the DAC output to provide a separate stable ground for the ECG module.
- Output bio-data over Wi-Fi.
- Provide an application for control over Wi-Fi.
- Make the wearable available as an independent device.

## Phase 2: independent hardware sequencer

- Develop a second device that can work independently from the wearable.
- When paired, receive wearable bio-data over Wi-Fi.
- Convert bio-data into sequences for synthesizers.
- Add physical controls.
- Add sequence visualization.
- Provide wired MIDI and CV outputs.

## Phase 3: standalone format

- Build the hardware sequencer as a compact standalone box.
- Use one encoder for unified adjustment.

## Phase 4: Eurorack format

- Build the hardware sequencer as a Eurorack module.
- Add physical controls and sequence visualization to the panel.
- Integrate it directly with modular synthesizers through MIDI and CV.

## v2.0 system

The wearable interface and hardware sequencer are two independent devices. The hardware sequencer will be produced in standalone or Eurorack format. When the two devices are paired, the wearable sends bio-data over Wi-Fi and the hardware sequencer turns it into MIDI/CV sequences for synthesizers.
