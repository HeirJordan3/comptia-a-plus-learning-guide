# Troubleshooting Display Issues

CompTIA A+ Core 1 — 220-1201  
Objective 5.3 — Given a scenario, troubleshoot video, projector, and display issues

## What You Need to Know

By the end of this lesson, you should understand how to approach:

- No signal / black screen basics (cable, power, input)
- Dim screens (brightness, OS auto-dim, backlight failure)
- VGA / generic video mode when Windows goes black after splash
- LCD projector bulbs, heat, fans, and filter cleaning
- Native resolution vs fuzzy / soft images
- Burn-in / image sticking and pixel shift
- Dead pixels
- Flashing screens
- Incorrect colors / night mode
- Monitor speaker / audio routing
- Flicker, bars, geometry, cables, and hardware acceleration
- Scaling vs resolution on high-DPI displays
- Severe LCD hardware failure vs cable/GPU/driver causes

## What Is It?

**Display troubleshooting** finds why a monitor, laptop screen, or projector will not show a clear, stable, correctly colored image — then fixes the cause.

Common devices:

- LCD monitors
- Laptop displays
- LCD projectors

## Why Does It Matter?

Displays are the main output users see all day. Tickets often start with:

- “No signal”
- Fuzzy text
- Flickering
- Wrong colors
- Dead pixels
- Projector will not stay on

Exam questions usually give a symptom and ask what to check next.

## Real-World Analogy

Think of a TV and a movie projector:

- Wrong input = HDMI cable in, but TV set to VGA
- Wrong resolution = stretching a photo until it looks soft
- Burn-in = a logo left on too long that ghosts forever
- Projector bulb = a very bright lamp that must cool down carefully

## How It Works

### No Signal / Black Screen — Start Simple

1. Confirm the **video cable** is fully seated on the PC **and** the monitor
2. Confirm the monitor has **power**
3. Set the monitor **input** to the port you are using (HDMI, DisplayPort, VGA, DVI, USB-C)
4. Adjust **brightness / contrast** if the image is extremely dim
5. Test with a **known-good monitor** or move this monitor to another PC

Many “dead display” tickets are cable, power, or wrong input.

### Video Until Windows, Then Black

If BIOS/POST and splash screens appear, then Windows goes black:

- Suspect OS display settings / drivers
- Try a **generic video mode** (historically Windows **VGA mode** via advanced boot / F8-era options — exact steps vary by Windows version)

Generic mode works with almost any monitor so you can fix resolution/drivers.

### LCD Projector Bulbs

LCD projectors use a very bright **metal halide** bulb.

| Fact | Why it matters |
| --- | --- |
| Bulb gets extremely hot (~1000°C inside) | Needs strong cooling |
| Fans run constantly | Move heat away from the bulb |
| Overheat sensors | Projector shuts down to protect the bulb |
| After shutdown, fans keep running | Cool the bulb gradually |
| Bulbs are expensive | Protect them with cool-down and clean filters |

When replacing a bulb (especially ceiling-mounted units):

- Follow the modular bulb swap process
- Clean dust and replace **air filters** so cool air can flow

### Native Resolution

An LCD has a fixed grid of pixels — the **native resolution** (horizontal × vertical).

| Setting | Result |
| --- | --- |
| OS matches native resolution | Sharpest text and graphics |
| OS uses a different resolution | Soft, fuzzy, stretched look |

If the image looks soft:

- Set the OS to the monitor’s native resolution
- Or use a compatible multiple of that resolution when needed

### Burn-In / Image Sticking

**Burn-in** (on LCDs often called **image sticking**) is a ghost of old content that stays after the image changes.

Common on always-on screens (menus, dashboards, departure boards).

Prevention / mitigation:

- Enable **pixel shift** (monitor slightly moves the image)
- For LCD sticking, try displaying a different image (for example a white screen) for a long period

More famous on old CRTs, but LCDs can show it too.

### Dead Pixels

A **dead pixel** stays black and does not light.

- Usually a manufacturing defect
- Cleaning the screen rules out dirt
- Cannot be fixed by cables or settings
- Fix = replace the display (if it bothers the user)

### Flashing Screen

Image drops out and returns.

Check:

1. Tight video connectors / try a new cable
2. Known-good monitor swap
3. OS is set for the correct monitor make/model
4. Display settings compatible with the monitor specs

### Incorrect Colors

Colors look too blue, too green, or otherwise wrong.

Check:

- Monitor tint / color presets / **factory reset**
- OS color settings
- **Night mode / night light** (shifts color temperature — bad for graphics/video work)

### Monitor Speakers / No Audio

If the display has speakers but sound is missing or quiet:

- Monitor volume / mute
- Audio input matches video path (HDMI audio with HDMI video)
- OS output device set to the HDMI/DisplayPort device
- Some monitors need video on HDMI + audio on a separate analog jack — configure both

### Dim Display

| Check | Note |
| --- | --- |
| Monitor brightness/contrast | First stop |
| OS auto-dim / adaptive brightness | Time of day or ambient light |
| Laptop on battery | Often dims to save power |
| GPU/driver brightness controls | Vendor control panels |
| Backlight failure | Bright and dark regions; may need parts or full replace |

### Flicker, Bars, Poor Geometry

For analog connections, check connector pins and seating.

Also try:

- Match **native resolution**
- Replace the video cable
- Disable **hardware acceleration** in the video driver if it causes artifacts (acceleration is faster but can glitch some setups)

### Scaling vs Resolution

| Problem | Fix |
| --- | --- |
| Tiny image centered on a large panel | Enable OS **display scaling** / stretch to fit |
| 4K native with unreadably small icons/text | Keep native resolution; raise scaling (100% → 200% → 300%) |

Scaling changes UI size without abandoning native sharpness.

### Severe LCD Artifacting

Heavy flicker, blocks, or lines across the whole screen often mean **LCD panel failure**.

Before replacing the panel:

- Swap the display cable
- Try another GPU / discrete adapter if present
- Update or change the video driver

Technicians may use **test patterns** to judge sharpness, color, and defect location.

## Side-by-Side Comparison

| Symptom | First useful checks |
| --- | --- |
| No signal / black | Cable, power, input select |
| Dim | Brightness, OS dimming, backlight |
| Soft / fuzzy | Native resolution |
| Ghost old UI | Burn-in / image sticking / pixel shift |
| One black spot | Dead pixel (clean first) |
| Flash on/off | Cable, monitor, OS display settings |
| Wrong tint | Monitor presets, night light |
| No sound from monitor | Volume + HDMI audio routing |
| Tiny UI on 4K | Scaling |
| Blocks / heavy lines | Cable → GPU/driver → panel replace |

## Key Terms

| Term | Meaning |
| --- | --- |
| Native resolution | Fixed pixel grid of an LCD |
| Burn-in / image sticking | Ghost of old content on screen |
| Pixel shift | Monitor moves image slightly to reduce burn-in |
| Dead pixel | Pixel stuck off (black) |
| Metal halide bulb | Bright projector lamp; runs very hot |
| VGA mode | Generic Windows video mode for troubleshooting |
| Hardware acceleration | GPU feature for faster drawing; can cause glitches |
| Scaling | Enlarge UI while keeping resolution |
| Backlight | Light source behind an LCD panel |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| No signal | Cable, power, wrong input |
| Fuzzy text | Not at native resolution |
| Always-on menu ghost | Burn-in / image sticking |
| One permanent black dot | Dead pixel |
| Projector shuts off hot / fans after off | Bulb protection cool-down |
| Replace projector lamp | Also clean filters |
| Colors weird at night | Night light / night mode |
| Monitor mute / HDMI audio | Output device + input match |
| Laptop dim on battery | Power-saving brightness |
| Artifacts after ruling out cable | GPU, driver, or panel |

## Common Mix-Ups

### Dead pixel vs dirt

Clean the screen before declaring a dead pixel.

### Resolution vs scaling

Wrong resolution looks soft. Tiny sharp UI needs **scaling**, not necessarily a lower resolution.

### Burn-in only on CRTs

LCDs can show image sticking too.

### Fans after projector “off” means broken

Cool-down is normal and protects the bulb.

### Black after Windows = dead monitor

If POST was visible, suspect OS video settings/drivers first.

## Quick Review

| Topic | Remember |
| --- | --- |
| No video | Cable → power → input → known-good display |
| Windows black after splash | Generic / VGA mode; fix drivers/settings |
| Projector | Hot bulb, fans, cool-down, clean filters |
| Sharpness | Match native resolution |
| Ghosting | Burn-in / sticking; pixel shift; long alternate image |
| Dead pixel | Replace display if it matters |
| Flash / flicker | Cable, monitor, settings, acceleration, panel |
| Color | Monitor reset + night mode check |
| Audio on monitor | Volume + correct digital/analog path |
| Size | Scaling for high-res readability |

---

## Continue Learning

- Previous Topic: [Troubleshooting Storage Devices](troubleshooting-storage-devices.md)
- Next Topic: [Troubleshooting Mobile Devices](troubleshooting-mobile-devices.md)
- Related: [Troubleshooting Hardware](troubleshooting-hardware.md)
- Related: [Display Attributes](../3-hardware/display-attributes.md)
- Back to [Domain 5 — Hardware and Network Troubleshooting](README.md)
