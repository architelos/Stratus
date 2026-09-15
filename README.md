# Stratus

My take on an custom, open source yet practical drone stack.

## Jett (ESC)

<p align="center">
  <img src="images/jett_front.jpg" width="48%">
  <img src="images/jett_back.jpg" width="48%">
</p>

**Current revision:** 2\
**Status:** Fabricating

### Specs

|                    |                                                    |
| ------------------ | -------------------------------------------------- |
| MCU                | STM32G071K(B/8)U(3/6)                              |
| Gate driver        | DRV8300DRGER                                       |
| PWM                | 48 kHz                                             |
| Input              | 2S to 4S LiPo                                      |
| Continuous current | 20 A continuous, 25A peaks                         |
| Current sensing    | High side hall effect sensor                       |
| Throttle interface | DShot / ... (standard protocols)                   |
| Telemetry          | Serial UART                                        |
| Capacitor bank     | 26 × 10 µF 0805 MLCC                               |
| PCB                | 38 x 41.5 mm, 30.5 × 30.5 mm mounting              |
| Copper             | 2 oz outer, 0.5 oz inner                           |

### Description

Built from the ground up to understand what is happening inside an ESC, rather than treating it as a black box. Stratus uses industry standard AM32 with custom firmware planned, and hardware designed around actually being able to inspect, modify, and learn from the system.

**Power tree:** `VBAT → 10V buck → 3.3V low-noise LDO` (The MOSFETs are driven by the 10V rail)

## FC

**Current revision:** TBD\
**Status:** Planned

The flight controller will complete the Stratus stack, with the same focus on practical hardware and understanding the underlying system.

## License

CERN-OHL-2.0, see [LICENSE](LICENSE)
