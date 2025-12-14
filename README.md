# Festival Drug Checking - NFC Tap Logger

Standalone NFC tap stations for tracking participant flow through festival drug checking services. Two Raspberry Pi Zero 2 stations log NTAG215 card taps to SQLite, enabling post-event wait time analysis.

## Quick Context

**Organization:** NUAA (NSW Users and AIDS Association)  
**Use case:** Festival harm reduction services - need to measure wait times and identify bottlenecks  
**Timeline:** First deployment in 2 weeks  
**Scale:** 50-500 people per event, 2-12 hour sessions  

## What It Does

1. Participant gets NFC card when they join queue
2. They tap card at each station (queue join, exit, etc.)
3. System logs timestamps automatically
4. After event: export data → analyze wait times in R

## Hardware

- 2× Raspberry Pi Zero 2 WH
- 2× PN532 NFC modules (I2C mode)
- 100× NTAG215 cards
- Power banks

## Key Goals

- **Reliable:** Works for full festival day without babysitting
- **Simple:** Peers can operate with minimal training
- **Offline-first:** No network dependency
- **Fast:** <2 sec from tap to confirmation

See `docs/` for full details.
