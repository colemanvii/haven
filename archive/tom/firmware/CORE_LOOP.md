# Core Loop

TOM firmware runs a single calm loop.

## States
- IDLE
- INPUT (wheel moved)
- BREATH (intentional delay)
- OUTPUT (text/glow update)
- RETURN (settle back to idle)

## Input
Wheel rotation produces discrete steps:
- direction: CW / CCW
- step_count: integer

## Timing
Intentional latency is applied on every user action:
- minimum delay: 120ms
- typical delay: 250–400ms
- maximum delay: 650ms

Delay may vary slightly to feel organic, but must remain predictable.

## Output
Two channels:
- Text: single line, updated only at OUTPUT
- Glow: ramps, never snaps

## Loop Rule
No state may trigger an interruptive behavior.
TOM only responds to direct interaction.
