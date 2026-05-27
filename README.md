# Orion Source of Truth Serial Interface for macOS

**Orion Source of Truth Serial Interface for macOS** is a public source-truth seed for building a native macOS serial communication layer for instrument workflows, beginning with the PLACO PLA unit.

## Current status

**Untested hardware seed.**

This repository is not yet verified against the physical PLACO PLA unit. It is being published openly so the architecture, assumptions, documentation, and test path are visible from the beginning.

Greg will mark this repository as tested only after he can connect the PLACO PLA unit, verify serial communication, capture real responses, and document the results.

## Purpose

This project exists to make instrument communication more inspectable, repeatable, and human-readable on macOS.

The goal is not to replace existing instrument ecosystems. The goal is to create a clean, native, source-truth interface layer that can help bridge:

- macOS
- Swift / SwiftUI
- serial devices
- PLACO PLA workflows
- SpatialAnalyzer-adjacent workflows
- metrology source packets
- reproducible test logs
- documented hardware communication

## Source-truth principles

- Do not claim hardware support before testing.
- Preserve real device responses.
- Log assumptions separately from facts.
- Keep test scripts simple.
- Make failures visible.
- Document serial settings, cables, adapters, drivers, timestamps, and device state.
- Treat the first successful connection as evidence, not magic.

## Initial target

PLACO PLA serial communication.

## Planned workflow

1. Identify serial adapter and device path.
2. Document cable / adapter / driver setup.
3. Open serial port from macOS.
4. Send minimal safe query command.
5. Capture raw response.
6. Save test log.
7. Generate source-truth packet.
8. Build SwiftUI cockpit once communication is verified.

## Untested disclaimer

This repository currently contains architecture notes and a test plan only. It should not be used as a validated production driver or confirmed PLACO PLA interface until hardware testing is complete.

## Design language

This belongs to the same family as:

- Orion Source of Truth
- Swifter
- OrionOS
- SA Cockpit
- source-truth metrology packets

The workflow is the evidence.
