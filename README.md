# CAN Bus CANH / CANL Waveform Visualizer

An interactive HTML widget that renders the differential CANH and CANL voltage waveforms for an 8-bit CAN bus data sequence.

## Files

| File | Description |
|------|-------------|
| `can_bus_canh_canl_waveform.html` | Self-contained interactive waveform visualizer |
| `README.md` | This file |

## Usage

Open `can_bus_canh_canl_waveform.html` in any modern browser — no server or dependencies required.

- **Toggle bits** — click any of the 8 bit buttons to flip between `0` (dominant) and `1` (recessive). The waveform updates immediately.
- **Randomize** — generates a random 8-bit pattern.

## CAN Bus Signal Levels (ISO 11898-2)

| State | CANH | CANL | Differential (CANH − CANL) |
|-------|------|------|---------------------------|
| Dominant (bit 0) | ~3.5 V | ~1.5 V | ~2.0 V |
| Recessive (bit 1) | ~2.5 V | ~2.5 V | ~0.0 V |
| Bus idle | ~2.5 V | ~2.5 V | ~0.0 V |

Receivers determine the bit value by measuring the differential voltage, which provides strong common-mode noise immunity.

## Features

- Interactive 8-bit sequence editor
- Accurate CANH / CANL voltage levels per ISO 11898-2
- Differential shading between the two lines
- Idle bus periods shown at start and end
- Responsive canvas — redraws on window resize
- Light and dark mode support via `prefers-color-scheme`

## Browser Support

Any modern browser with Canvas 2D API support (Chrome, Firefox, Safari, Edge).
