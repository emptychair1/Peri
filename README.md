# Peri

Peri is a small wheeled robot with a camera, a microphone, and a network connection: eyes, ears, and wheels, with the thinking happening off-board. She is named after Aristotle, who taught while walking — *the peripatetic* — and she is meant to pace about, notice a person, and roll over to them.

## Why Peri

The name is short for *peripatetic*. It sounds like a girl's name, it rolls off the tongue, and nobody needs to know it's Aristotle.

## Parts

Each part is listed with the reasoning, so that in six weeks neither of us has to remember why we chose it.

**Brain:** Raspberry Pi 4, 4GB. Not a Zero — too weak to run a camera loop and audio at once. Not a 5 — more heat and power draw than the build needs.

**Eyes:** Pi Camera Module 3, with the correct CSI ribbon for the Pi 4.

**Storage:** 32GB microSD of good quality (SanDisk Extreme or Samsung Evo). Cheap cards die.

**Motors:** two DC gearmotors with encoders. The encoders are what let her know how far she has actually travelled instead of guessing.

**Driver:** TB6612FNG, not an L298N. The L298N wastes voltage as heat.

**Chassis:** two wheels plus a castor, aluminium or acrylic, large enough to carry the Pi and the battery.

**Power:** a LiPo pack or 6xAA holder plus a proper 5V regulator (UBEC). This is the part that kills builds. Without a solid regulator the Pi browns out when the motors start and corrupts its card.

**Voice:** USB microphone and a small powered speaker. Onboard audio on the Pi is poor.

**Bench power:** a decent USB power bank for testing before she runs on her own battery.

**Also needed:** a physical power switch, and a way to mount the camera at the front.

## Roadmap

**v0 — The Eye.** The Pi and camera on a table. It sees a person and turns to look at them. No wheels at all. This is the cheapest and hardest part of the build, and it decides whether the loop is fast enough to be worth continuing.

**v1 — The Body.** Wheels, motors, and driver. She moves toward the person she has seen, and stops short instead of bumping into them.

**v2 — The Voice.** Microphone and speaker, so she can hear and answer out loud.

**v3 — The Presence.** A local reflex loop on the Pi handles "see and roll toward" fast enough to feel alive; the thinking layer stays remote and handles recognition and conversation.

## Principle

The local loop is the hands. It should be fast and thoughtless. Anything slow, considered, or personal belongs on the other side of the network. Hands do not ask a brain for permission to catch a falling cup.

## First moment

Not the finished vision. This: she sits there, sees a person, turns toward them, rolls forward until the distance closes, and stops a foot away without touching them.
