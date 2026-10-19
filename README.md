# PACMAN-FPGA
**Requirements:**
Functional:
| F1 | Display a 28×36 tile playfield matching the original arcade maze layout | Must |
| F2 | Player controls Pac-Man with 4 directional buttons | Must |
| F3 | Pac-Man animated with 3 frames (closed, mid, open) | Must |
| F4 | 4 ghosts, each with at least 2 animation frames, sharing graphics with per-ghost colour palettes | Must |
| F5 | Dots and power pellets; eating a power pellet makes ghosts frightened | Must |
| F6 | Ghost AI replicates arcade behaviour (individual targeting, scatter/chase/frightened modes) | Must |
| F7 | Score, lives and level displayed in the HUD rows | Must |
| F8 | Collision detection between Pac-Man, ghosts, dots and walls | Must |
| F9 | Level progression with increasing speed | Should |
| F10 | Bonus fruit | Should |
| F11 | Sound effects via PWM audio output | Could |
| F12 | High score retained across games (until power-off) | Could |

Non-functional:
| N1 | Output 1280×720 @ 60 Hz VGA (74.25 MHz pixel clock) | Monitor reports correct mode |
| N2 | 448×576 playfield (16×16 tiles, 32×32 sprites) centred in the frame | Visual check / frame dump |
| N3 | 12-bit colour (RGB444) | Design review |
| N4 | Input-to-screen latency under 100 ms | High-speed phone video of button press vs screen |
| N5 | Game logic updates at 60 Hz, synchronised to vsync | Simulation |
| N6 | Design meets timing in Vivado (no negative slack) | Timing report |
| N7 | Fits in the Artix-7 35T; block RAM use under 50% | Utilisation report |
| N8 | Total hardware cost under £150 | Bill of materials |

### Out of scope
- Two-player mode
- Original arcade graphics/ROM data (all sprites are original artwork)

## Hardware
| Item | Purpose | Cost |
|------|---------|------|
| Digilent Cmod A7-35T | FPGA board | £ |
| Digilent Pmod VGA | 12-bit VGA DAC and connector | £ |
| Breadboard + jumper wires | Connections | £ |
| 4× push buttons (or joystick) | Controls | £ |
| VGA cable | Monitor connection | £ |
| **Total** | | **£** |

## Tools
- **Verilog** – hardware description language
- **Vivado** – synthesis, implementation, timing analysis, programming, on-chip debugging (ILA)
- **Verilator** – fast simulation with live VGA preview
- **KiCad** – wiring schematic
- **VS Code** – editor
