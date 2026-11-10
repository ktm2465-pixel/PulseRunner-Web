# Pulse Runner: Heartline — Web Portfolio Build

Playable Unity 6000.3.14f1 prototype. This repository contains the browser build only, not the private Unity source project.

## Play

https://ktm2465-pixel.github.io/PulseRunner-Web/

Wait for loading, read **조작 방법**, then click **게임 시작**. PC Chrome / Edge recommended.

| Input | Action |
|---|---|
| A / D | Move, Tube rotation, Rail balance |
| Left mouse | Pulse |
| Space | Jump / contextual Vault or Rail entry |
| W + A / D hold | Wall Run |
| W + opposite direction + Space | Wall Jump |
| S / Left Shift | Slide / Dash |
| P / R | Pause-resume / Restart |

The game auto-runs. W is not forward movement or acceleration. Release the requested key to finish Hold actions.

## Verification

### Consecutive input / rail direction fix

- A Release or unrelated key can no longer reuse a previous Press to consume the next Tap.
- Rail directions use ASCII `<<` / `>>` and an explicitly assigned built-in font/material.
- Regression reproduction: 2 tests failed before the fix, passed afterward.
- Windows-target EditMode: 681/681 passed. Web-target EditMode: 678/681; three PC-specific audio sample/endpoint checks differ after web import.
- Timing windows and DSP clock are unchanged. Dense manual input and rail visibility still require browser play checks.

- Unity WebGL build: succeeded.
- Local Chromium browser: loading, start, D movement, P pause/resume and R restart checked.
- No browser console errors during the checked segment; missed inputs produced expected gameplay collision/recovery warnings.
- Full-song manual play, audio latency calibration and mobile device support require separate testing.

Artwork, audio and other game assets are supplied for this portfolio demo. No general redistribution license is granted.
