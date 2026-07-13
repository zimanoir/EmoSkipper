# pulseFlesh v2.0

A wireless wearable bio-sequencer and bio-data source for musical, stage, and interactive systems.

## Project direction

**pulseFlesh v2.0** grows out of an experimental bio-interface NIME that transforms body signals into musical control data. The current hardware is at the stage-testing phase. Artistic work with the prototype created the need to reconfigure the project as a wireless instrument: a wearable bio-sequencer and a source of bio-data rather than a device tied directly to one synthesizer by cables.

The v2.0 system is developing into a wearable interface that reads heart activity through ECG and sends the resulting data wirelessly over Wi-Fi MIDI.

The wearable interface will work with either of two optional output devices:

1. **Standalone box** — a compact external unit with wired MIDI and CV outputs, adjusted through a single encoder.
2. **Eurorack module** — a dedicated module with MIDI and CV outputs for direct integration with modular synthesizers.

The wearable unit will also be usable independently as a complete wireless bio-sequencer and bio-data source with access to an application.

## System path

```text
reusable metal connectors
        ↓
ECG module
        ↓
wearable ESP32-D + DAC output
        ↓
Wi-Fi MIDI
        ├──→ application / musical or stage software
        ├──→ optional standalone box → wired MIDI + CV
        └──→ optional Eurorack module → MIDI + CV
```

The ESP32-D wearable board uses a DAC output to provide a separate stable ground for the ECG module and to make the interface convenient to wear.

## Current status: stage testing

The current prototype is almost fully soldered and is being tested in a stage context. It reads body signals — heart activity via ECG, muscle tension, and physical impacts — and converts them into control voltages for analog synthesizers.

At this stage, the prototype works as a chaotic noise machine and vibe generator, combining structured heartbeat data with unpredictable muscle activity. Stage testing is guiding its artistic transformation into the wireless v2.0 bio-sequencer.

## Current prototype features

- **ECG input** — reads heart activity and converts it to smooth CV modulation.
- **Muscle sensing** — detects muscle tension as a chaos index for expressive control.
- **Impact detection** — uses a piezo sensor for physical hits and sharp CV triggers.
- **Three independent outputs** — Mix 1, Mix 2, and Direct Piezo.
- **Low-latency processing** — approximately 450 Hz loop speed.
- **Upcycled design** — uses salvaged components from broken electronics.

## v2.0 wearable interface

- Reusable metal connectors.
- ESP32-D board worn on the body.
- DAC output providing a separate stable ground for the ECG module.
- Wireless MIDI transmission over Wi-Fi.
- Access to an application.
- Independent use as a complete wireless bio-sequencer and bio-data source.
- Availability as a separate wearable device.

## Optional output devices

### Standalone box

- Wired MIDI output.
- CV outputs.
- Unified adjustment with one encoder.

### Eurorack module

- MIDI output.
- CV outputs.
- Direct integration with modular synthesizers.

## Current stage-prototype specifications

| Aspect | Details |
|--------|---------|
| **Microcontroller** | ESP32 |
| **ECG Sensor** | AD8232 Red Board |
| **Power** | 18650 Battery + Charging Board |
| **Outputs** | 3× CV (1kΩ buffered) |
| **Loop Speed** | ~450 Hz |
| **ADC Resolution** | 12-bit |

These specifications describe the current stage prototype. The v2.0 wearable and its optional output devices are the next development stage.

## Integration

One pulseFlesh integration is **Dance of Life**, which uses Max/MSP and MediaPipe. Heart rhythm can be used there as a musical and rhythmic control signal alongside other input data.

## Quick links

- 📖 **[Full documentation](documentation/)** — project overview and signal processing.
- 🧭 **[Development roadmap](documentation/roadmap.md)** — path from stage prototype to v2.0.
- 🔧 **[Building instructions](documentation/BUILDING.md)** — current prototype assembly.
- ⚙️ **[Hardware](hardware/)** — current prototype schematic and components.
- 💾 **[Firmware](software/)** — ESP32 Arduino sketch.
- 🎧 **[Listen](https://on.soundcloud.com/DI3SJaFWWPOsZSelK7/)** — stage-prototype test recording with a CV-controlled Moog Werkstatt-01.

## Project structure

```text
.
├── README.md
├── CITATION.cff
├── hardware/
├── software/
├── documentation/
├── images/
└── files/
```

## Author

**Fëdor Zima** — Conservatorio Maderna-Lettimi Cesena Rimini

## License

MIT License — feel free to use, modify, and share.

## Citation

If you use pulseFlesh v2.0 in your work, please cite it using the metadata in [`CITATION.cff`](CITATION.cff).

---

**Status:** Stage testing / v2.0 wireless redevelopment<br>
**Last updated:** July 2026
