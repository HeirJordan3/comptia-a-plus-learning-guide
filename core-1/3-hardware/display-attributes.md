# Display Attributes

CompTIA A+ Core 1 — 220-1201  
Objective 3.1 — Displays

## What You Need to Know

By the end of this lesson, you should understand:

- What pixel density (PPI) means and how size affects it
- How refresh rate (Hz) relates to smooth motion
- Why the GPU and cable must support the refresh rate
- What screen resolution means (for example HD vs 4K)
- What color gamut is and why it matters for graphics work

## What Is It?

Display attributes are the technical specs that differentiate one monitor from another.

This lesson covers:

- Pixel density
- Refresh rates
- Screen resolution
- Color gamut

The best monitor depends on the job: gaming, video, presentations, lobby signage, or everyday office use.

## Why Does It Matter?

Help desk and IT support often help users choose or troubleshoot displays:

- “Why does this big TV look less sharp than my desktop monitor?”
- “Gaming looks stuttery.”
- “Graphics colors look off on this screen.”
- “I bought a 144 Hz monitor, but it still feels like 60 Hz.”

Understanding specs helps you match the display to the task and check the whole path: monitor, video card, and cable.

## Real-World Analogy

Think of a display like a flipbook:

- **Resolution** = how detailed each page is drawn  
- **Pixel density** = how tightly those details are packed into a small area  
- **Refresh rate** = how fast you flip the pages  
- **Color gamut** = how many paint colors are in the box  

A big flipbook with the same drawing detail spread out looks less crisp up close. Slow flipping looks choppy. A small paint set cannot match a professional art kit.

## How It Works

### Pixel Density

**Pixel density** is how many pixels fit in 1 inch of screen area (pixels per inch, or **PPI**). In some regions this may be measured per centimeter.

Higher pixel density usually means a sharper, clearer image.

Screen vs print:

- Screens are often discussed in PPI
- Printers use **DPI** (Dots Per Inch)
- If you print what you see on screen, printer DPI must be able to represent the image well

#### Same Resolution, Different Clarity

Pixel density depends on both resolution and physical size.

Example from the lesson: a **4K** display has **3,840** horizontal pixels.

| Display | Approx. width | Math idea | Approx. PPI |
| --- | --- | --- | --- |
| 27-inch 4K | ~24 inches wide | 3840 ÷ 24 | ~160 PPI |
| 65-inch 4K | ~57 inches wide | 3840 ÷ 57 | ~67 PPI |

Same resolution, very different pixel density. The smaller screen packs the same pixels into less space, so it looks sharper.

Simple idea: PPI ≈ horizontal pixels ÷ width in inches (for U.S. inch-based examples).

### Refresh Rate

A display shows a series of images refreshed many times per second.

**Refresh rate** is measured in **hertz (Hz)** — cycles per second.

People sometimes say **FPS** (Frames Per Second). With **V-sync** enabled, Hz and FPS can match. Some configurations may update only part of the screen each cycle, so they are not always identical.

Typical content speeds:

| Content | Common rate idea |
| --- | --- |
| Movies (U.S.) | About 24 FPS |
| TV / online video | About 30 FPS |
| Sports / gaming | 60 FPS or higher |

Low refresh rates look choppy. High refresh rates look smoother, especially for fast motion.

The display is only one part of the path. You also need:

- A video card / GPU that can drive that rate
- A cable / connection that supports it

Examples from the lesson:

| Connection | Capability idea |
| --- | --- |
| HDMI 2.1 | 4K at up to 144 Hz |
| DisplayPort 2.1 | Dual 4K, each up to 144 Hz |

A 144 Hz monitor still cannot deliver 144 Hz if the adapter or cable cannot support it.

### Screen Resolution

**Resolution** is the number of pixels across the width and height of the display.

More pixels on the same physical size usually means a sharper image.

Common comparison from the lesson:

| Name | Resolution |
| --- | --- |
| HD | 1920 × 1080 |
| 4K | 3840 × 2160 |

Many standards use a **16:9** aspect ratio, but other ratios exist. Choose what fits the use case. Some monitors also use nonstandard resolutions.

### Color Gamut

The human eye can see a wider range of colors than most displays can show.

**Color gamut** is the range of colors a display can reproduce.

This matters most for graphics and image work, where a wider, accurate gamut is valuable.

Common reference standards you may see in specs:

| Standard | Notes |
| --- | --- |
| sRGB | Standard Red Green Blue; common baseline |
| Adobe RGB | Broader professional color space |
| Rec. 709 / DCI-P3 / ITU standards | Other common comparison targets |

Specs often list percentages, such as:

- 100% sRGB
- 95% sRGB
- 100% Rec. 709
- 98% DCI-P3

You do not need every standard memorized. Compare the percentages to the job:

- Web / email → a slightly lower sRGB percentage may be fine
- Graphics / video editing → aim closer to 100% of the needed standard

OLED displays often provide strong color representation and better match to these standards than many traditional LCDs. IPS LCD panels can also reach high sRGB coverage.

## Key Terms

| Term | Meaning |
| --- | --- |
| Pixel density / PPI | Pixels per inch; clarity of the image on screen |
| DPI | Dots per inch; printer resolution measure |
| Refresh rate / Hz | How many times the screen refreshes per second |
| FPS | Frames per second |
| V-sync | Syncs frame output to refresh rate |
| Resolution | Pixel count width × height |
| HD | 1920 × 1080 |
| 4K | 3840 × 2160 |
| Aspect ratio | Width-to-height proportion (often 16:9) |
| Color gamut | Range of colors a display can show |
| sRGB | Common standard color space |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Pixels in one inch of screen | Pixel density / PPI |
| Same 4K on huge TV looks less sharp | Lower PPI from larger size |
| Smooth gaming / sports motion | Higher refresh rate |
| Choppy motion on fast content | Refresh rate too low |
| 144 Hz monitor still capped | Check GPU and cable |
| 1920 × 1080 | HD |
| 3840 × 2160 | 4K |
| Range of displayable colors | Color gamut |
| Graphics editing needs accurate color | Wide / high % color gamut |
| Best color match often | OLED (strong representation) |

## Common Mix-Ups

### Resolution vs Pixel Density

- Resolution = total pixels (for example 3840 × 2160)
- Pixel density = how tightly those pixels are packed into the physical screen

### Hz vs FPS

- Hz = display refresh cycles
- FPS = frames produced/shown
- They can match with V-sync, but they are not always the same

### Monitor Spec vs Full Path

Buying a high-refresh monitor is not enough. The GPU and connection must support it too.

### PPI vs DPI

- PPI = screen clarity measure
- DPI = printer dots measure

### Color Gamut vs Panel Type Alone

Panel type (IPS, OLED, etc.) matters, but gamut percentages in the specs tell you how much of a color standard the display covers.

## Quick Review

| Attribute | Remember |
| --- | --- |
| Pixel density | Higher PPI = sharper look |
| Size + resolution | Bigger screen, same pixels → lower PPI |
| Refresh rate | Higher Hz = smoother motion |
| Full path | Monitor + GPU + cable |
| Resolution | HD 1920×1080; 4K 3840×2160 |
| Color gamut | Range of colors; check % of standards |

---

## Continue Learning

- Previous Topic: [Display Types](display-types.md)
- Next Topic: [Network Cables](network-cables.md)
- Related: [Video Cables](video-cables.md)
- Back to [Domain 3 — Hardware](README.md)
