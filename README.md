# P9981 ZMK Keymap — BlueBerry Android Layout

A ZMK keymap for the P9981 keyboard, based on the "BlueBerry" Android layout by Drexel Macintosh.

---

## Layers

The keyboard has 4 layers:

| # | Name    | How to reach                        |
|---|---------|-------------------------------------|
| 0 | DEFAULT | Always active at base               |
| 1 | SYM     | Tap `ALT` (sticky) or hold for lock |
| 2 | UPPER   | Double-tap `ALT` from SYM layer     |
| 3 | MEDIA   | Double-tap `SYM` from UPPER layer   |

---

## Layer 0 — DEFAULT

The main typing layer. Every letter key supports **hold for uppercase** (hold = capital, tap = lowercase).

```
┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┐
│  Q  │  W  │  E  │  R  │  T  │  Y  │  U  │  I  │  O  │  P  │
│ (Q) │ (W) │ (E) │ (R) │ (T) │ (Y) │ (U) │ (I) │ (O) │ (P) │
├─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┤
│  A  │  S  │  D  │  F  │  G  │  H  │  J  │  K  │  L  │  ←  │
│ (A) │ (S) │ (D) │ (F) │ (G) │ (H) │ (J) │ (K) │ (L) │BSPC │
├─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┤
│ ALT │  Z  │  X  │  C  │  V  │  B  │  N  │  M  │ STP │ ENT │
│     │ (Z) │ (X) │ (C) │ (V) │ (B) │ (N) │ (M) │LG(N)│     │
└─────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┘
         ┌──────┬──────────┬─────────┬──────┬───────┐
         │ SHFT │  0/PWR   │  SPACE  │ EALT │ LCTRL │
         └──────┴──────────┴─────────┴──────┴───────┘
```

**Key notes:**
- **Hold any letter** → types the uppercase version
- **ALT** — tap for sticky SYM layer, double-tap to lock into SYM layer
- **SHFT** — tap for sticky shift, double-tap for Caps Lock
- **EALT** — tap for sticky Right Alt, double-tap to hold Right Alt
- **0/PWR** — tap for `0`, hold for power key (`K_PWR`) with Win+A
- **STP/LG(N)** — tap for media stop, hold for Win+N

---

## Layer 1 — SYM (Symbols & Numbers)

Reached by tapping `ALT` on the default layer. Tap = sticky (one shot), double-tap = locked.

```
┌──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┬──────┐
│  #   │  1   │  2   │  3   │  (   │  )   │  _   │  -   │  +   │  @   │
│  (~) │(HOM) │ (UP) │(PGU) │  [   │  ]   │  <   │  >   │  ^   │  %   │
├──────┼──────┼──────┼──────┼──────┼──────┼──────┼──────┼──────┼──────┤
│  *   │  4   │  5   │  6   │  /   │  :   │  ;   │  '   │  "   │  DEL │
│  (=) │(LFT) │ (DN) │(RGT) │  \   │  |   │  &   │  '   │  "   │  ←   │
├──────┼──────┼──────┼──────┼──────┼──────┼──────┼──────┼──────┼──────┤
│ UPPR │  7   │  8   │  9   │  ?   │  !   │  ,   │  .   │  $   │ ENT  │
│      │(END) │ (DN) │(PGD) │  {   │  }   │  `   │  .   │ PSCRN│      │
└──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┘
         ┌──────┬──────────┬─────────┬──────┬───────┐
         │ SHFT │  0/EP_ON │  SPACE  │ EALT │ LCTRL │
         └──────┴──────────┴─────────┴──────┴───────┘
```

**Key notes:**
- Each key: **tap** = bottom symbol, **hold** = top symbol/action
- **UPPR** (col 1, row 3) — tap to return to DEFAULT, double-tap to go to UPPER layer
- **0/EP_ON** — tap for `0`, hold to force backlight power on

---

## Layer 2 — UPPER

Reached by double-tapping `ALT` from the SYM layer. Functions as a shifted/caps version of the default layer — all letters type as-is (no hold-for-caps needed here).

```
┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┐
│  Q  │  W  │  E  │  R  │  T  │  Y  │  U  │  I  │  O  │  P  │
├─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┤
│  A  │  S  │  D  │  F  │  G  │  H  │  J  │  K  │  L  │  ←  │
├─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┤
│MEDIA│  Z  │  X  │  C  │  V  │  B  │  N  │  M  │  $  │ ENT │
└─────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┘
    ┌──────┬──────────┬─────────┬──────┬───────┐
    │ SHFT │  0/EP_ON │  SPACE  │ EALT │ LCTRL │
    └──────┴──────────┴─────────┴──────┴───────┘
```

**Key notes:**
- Plain letter keys — no hold-for-caps, just direct output
- **MEDIA** (col 1, row 3) — tap to return to DEFAULT, double-tap to go to MEDIA layer

---

## Layer 3 — MEDIA

Reached by double-tapping `MEDIA` from the UPPER layer. Handles Bluetooth, backlight, and system controls.

```
┌──────┬──────┬────────┬────────┬──────────┬──────┬──────┬──────┬──────┬──────┐
│ BT 0 │ BT 1 │ BT CLR │  RST   │  EXT PWR │      │      │      │      │      │
├──────┼──────┼────────┼────────┼──────────┼──────┼──────┼──────┼──────┼──────┤
│ BT 2 │ BT 3 │        │        │          │      │      │      │      │      │
├──────┼──────┼────────┼────────┼──────────┼──────┼──────┼──────┼──────┼──────┤
│ BACK │      │        │        │  BL DEC  │ RGB  │BL INC│      │ BOOT │      │
└──────┴──────┴────────┴────────┴──────────┴──────┴──────┴──────┴──────┴──────┘
         ┌──────────┬──────┬──────────────┬──────┬──────┐
         │  TO: 0   │      │  OUT TOGGLE  │      │      │
         └──────────┴──────┴──────────────┴──────┴──────┘
```

**Key notes:**
- **BT 0–3** — connect exclusively to Bluetooth device 0–3 (disconnects all others)
- **BT CLR** — clear all Bluetooth pairings
- **EXT PWR** — toggle external power (backlight power rail)
- **BL DEC / BL INC** — decrease / increase backlight brightness
- **RGB** — toggle RGB underglow
- **BOOT** — put keyboard into bootloader mode
- **OUT TOGGLE** — toggle between USB and Bluetooth output
- **BACK / TO: 0** — return to DEFAULT layer

---

## Special Behaviors

### Tap Dance
Keys that behave differently on single vs double tap:

| Key   | Single Tap         | Double Tap         |
|-------|--------------------|--------------------|
| ALT   | Sticky SYM layer   | Lock into SYM layer |
| SHFT  | Sticky Shift       | Caps Lock          |
| EALT  | Sticky Right Alt   | Hold Right Alt     |
| UPPR  | Back to DEFAULT    | Go to UPPER layer  |
| MEDIA | Back to DEFAULT    | Go to MEDIA layer  |
| BACK  | Back to DEFAULT    | Back to DEFAULT    |

### Hold-Tap (mtt)
All letter keys on the DEFAULT and SYM layers use hold-tap:
- **Tap** → lowercase letter / primary symbol
- **Hold** → uppercase letter / secondary symbol

Timing: 200ms tapping term, 125ms quick-tap and prior-idle threshold.

### Sticky Keys
- **SHFT** — after tapping, the next key press is shifted, then it releases
- **EALT** — after tapping, the next key press uses Right Alt, then releases
- **LCTRL** — sticky Left Control (one-shot)

Both sticky keys release after **2500ms** if no key is pressed.

---

## Backlight & RGB

- Backlight turns on automatically at boot at **40% brightness**
- Auto-off after **30 seconds** of idle
- Brightness step: **10%** per press of BL INC / BL DEC (MEDIA layer)
- RGB underglow toggle also on MEDIA layer
- Holding `0` on the SYM or UPPER layer bottom row forces backlight power on (`EP_ON`)
