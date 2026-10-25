---
title: LOTUS
aliases: [Lighted Overnight Transtibial Universal Socket, senior design project]
tags: [project, prosthetics, senior-design]
status: active
updated: 2026-10-25
---

# LOTUS

LOTUS (Lighted Overnight Transtibial Universal Socket) is a nighttime
prosthesis for transtibial users, built as a senior design project.

## Current state
- **Socket:** 4-petal design, current revision Alpha.3, with a distal base cup. The back petal opens on a torsion spring when the socket comes off, which presses a normally closed switch to turn the light off.
- **Light:** the pylon is wrapped in a 12 V LED strip, powered by a battery or power bank. There is no path light and no IMU.
- **Limb contact:** silicone pads (medical-grade gel-liner silicone) bonded to each petal with mushroom-style anchors.
- **Distal cushion:** 85A TPU, printed with 2 walls and 8% gyroid infill. It is for comfort and is not load-bearing.
- **Distal attachment:** Bulldog TD-P21 titanium 4-hole pyramid outside the cup, an aluminum puck screw block inside, and an Anclote suction plate.
- **Hinges:** M2 screws into brass inserts on the cup.
- **Materials:** PETG for test parts; final prototype in PAHT-CF or Nylon CF.

## FEA
- **Repository:** [LOTUS FEA](https://github.com/Shim-1122/LOTUS-FEA), public. It holds the FEBio 4.13 model of a below-knee limb (skin, fat, muscle and four bones, built as CAD from approximations of an MRI scan) inside the 4-petal socket.
- **Results:** at the 75 N example lace tension, max tissue displacement is 6.5 mm, peak contact pressure 57 kPa and total contact force 560 N. The run converged through a 2 mm pull-out with 8% of the contact area slipping. These are numbers from a model, not clinical validation.
- **Still needed:** a RevoFit strand rating with its source, socket CAD and lace routing, a compression test of the printed cushion, and confirmation of the bone labels.

## Decisions
- 2026-10-25: Open-source FEA repo named LOTUS FEA (working title was Knee FEA). The segmented limb and bone STLs are published in it.
- 2026-10-25: The socket has 4 petals, not 6.
- 2026-10-25: Pads are modelled as gel-liner silicone (shear modulus 23 kPa, Sanders 2004). The cushion is modelled as 85A TPU gyroid at 8% infill (homogenised E about 71 kPa).
- 2026-10-25: The FEA site will be hosted on a subdomain of Shyam's Vercel domain.

## Links
- [[Rules]]
- [[Log/2026-10]]
