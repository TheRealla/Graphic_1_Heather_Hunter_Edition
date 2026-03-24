# Graphic_1 — Heather Hunter Edition

**SEALS ESTATE — PRECISION SYNTHESIS ENGINE (PROMPT 57)**  
**"GraphicHBridgeHeather" — DANCER + ICON + VIVID CUT + BEZIER MORPH**  
*1978 Mode Aware • Fully Evolved with Bézier Curves & Performance Hacks*

A single-voice digital oscillator that transforms from pristine high-fidelity sine into raw, soulful 8-bit 1978-era grit — all controlled by one magical parameter: **Digital Pressure**.

This is the definitive **Heather Hunter Edition v2.0** — now running natively in **Cmajor**, with full cubic Bézier control over waveform, saturation, bit-depth morph, and pressure response.

![Bézier Dancer Waveforms](assets/bezier_plot.png)  
*(Time-domain comparison + pressure-mapped curves — generated live from the engine)*

## Highlights

- Bézier-Powered Dancer — artistic cubic Bézier waveforms (Clean, 1978 Grit, Heather Signature presets)
- Non-linear Bézier Mappings for bit-depth, magnetic saturation, and pressure response
- Vivid Cut one-pole HPF for clean, punchy output with no DC mud
- Pressure-linked Sample-Rate Reduction (1× to 16×) for crunchy early-digital character
- Performance optimizations: cached pow(), reduced branching, clamp-only math, SIMD-ready
- Native Cmajor implementation — runs extremely fast in Cmajor Studio, WebAudio, VST3, AU, AAX and more
- Built-in Faux Encryption Tests for reversible state scrambling (fun testing layer with 1978 paranoia vibe)

## What is Faux Encryption?

A playful, reversible scrambling layer inspired by vintage DSP tricks.  
It “encrypts” internal state (phase, heldSample, filter memory) using a simple chaotic transform, then decrypts it back.  
Used for round-trip verification tests and to add a classified SEALS ESTATE flavor.  
See the test file for full details and verification (max error stays within float precision).

## Quick Start

1. Download and open **Cmajor Studio** (free from cmajor.dev)
2. Create a new patch
3. Copy the content of GraphicHBridgeHeather.cmajor into the processor
4. Play the patch and adjust **Digital Pressure** (0.0 = clean, 1.0 = full Heather grit)
5. Switch Preset (0 = Clean, 1 = 1978, 2 = Heather)

To build as a VST3/AU plugin:
cmaj generate --target=vst3 GraphicHBridgeHeather.cmajor --output=build

## Parameters

- frequency:        20–20000 Hz (default 440)
- digitalPressure:  0.0 – 1.0 (default 0.3)
- preset:           0–2 (default 2 = Heather Signature)

## Files

- GraphicHBridgeHeather.cmajor          Main processor with all enhancements
- tests/faux_encryption_test.cmajor     Reversible encryption round-trip test
- assets/bezier_plot.png                Visual reference of the Bézier curves
- examples/                             Additional patches (unison, modulated pressure, etc.)

## Enhancements Summary (v2.0)

- Full cubic Bézier waveform generation
- Bézier curves for every internal mapping (bit-depth, saturation, pressure)
- Cached expensive math operations
- Branch-light and clamp-only code for maximum performance
- Faux encryption test layer
- Native Cmajor format for speed and portability

## License

MIT License — feel free to use, modify, and include in commercial projects.

---

Made for those who want digital that feels analog… in all the wrong (right) ways.

**Repository**: https://github.com/TheRealla/Graphic_1_Heather_Hunter_Edition  
**Version**: Heather Hunter Edition v2.0 — March 2026

Now go make some sounds that hurt so good.


Understood. We’ll leave the documentation in the hands of Providence and the future. When the time is right, we can formalize the **SEALS ESTATE Machine Law Protocol** and the technical manual for the **Amorph-Graphic 1** interface.

For now, I have concentrated the "Expensive" DSP logic into a structural overview of the **16-Harmonic Timbre Map**. This will serve as the mathematical backbone for when you return to the Cmajor implementation.

---

### **THE ARCHITECTURAL CORE: 16-PARTIAL ADDITIVE STRATEGY**

To maintain the **German Precision** and **Graphic 1** discipline, the synthesis engine operates on a fixed-ratio harmonic grid. Each partial is treated as a discrete geometry.

| Partial | Ratio | Character | "Expensive" Scaling |
| :--- | :--- | :--- | :--- |
| **1** | $1f$ | **The Root** | Fundamental weight; pure sine; 0.0dB ref. |
| **2** | $2f$ | **The Octave** | Adds "expensive" hollow warmth. |
| **3** | $3f$ | **The Fifth (+1 Oct)** | Clarifies the pitch center. |
| **4** | $4f$ | **The Double Octave** | Adds "sheen" and "air." |
| **5-16** | $5f \dots 16f$ | **The Texture** | Where the "Digital Pressure" creates the edge. |

---

### **THE H-BRIDGE "ICON" SWITCHING LOGIC**

The transition from the **Dancer** (additive sum) to the **Icon** (H-Bridge output) follows a **Transcendental Hysteresis** curve. This prevents the "cheap" sound of linear clipping.

> **Mathematical Identity:** > Instead of $y = \text{sign}(x)$, we use a **Soft-Switching Sigmoid**:
> $$y = \frac{x}{\sqrt{1 + x^2}}$$
> This ensures that even when the H-Bridge "switches," the transitions contain high-frequency musical information rather than just DC square-wave noise.

---

### **NEXT STEPS FOR THE REALLA / SEALS ESTATE**

When you are ready to move from philosophy to the final build, I can help you with:

1.  **The Cmajor "Partial Array"** – A vectorized loop that calculates all 16 partials with independent amplitude curves.
2.  **The GUI Mapping** – Translating mouse-coordinates (drawn pixels) into 10-bit frequency words for the 1978-style DCO logic.
3.  **The Scaling Filter** – Implementing a surgical 31-EDO / 53-EDO quantizer for the pitch curves.

**Would you like me to hold these DSP specifications in the project memory for when you're ready to continue?**
