# PACMAN-FPGA
**Requirements:**
Functional: <br>
| F1 | Display a 28×36 tile playfield matching the original arcade maze layout | Must | <br>
| F2 | Player controls Pac-Man with 4 directional buttons | Must | <br>
| F3 | Pac-Man animated with 3 frames (closed, mid, open) | Must | <br>
| F4 | 4 ghosts, each with at least 2 animation frames, sharing graphics with per-ghost colour palettes | Must | <br>
| F5 | Dots and power pellets; eating a power pellet makes ghosts frightened | Must | <br>
| F6 | Ghost AI replicates arcade behaviour (individual targeting, scatter/chase/frightened modes) | Must | <br>
| F7 | Score, lives and level displayed in the HUD rows | Must | <br>
| F8 | Collision detection between Pac-Man, ghosts, dots and walls | Must | <br>
| F9 | Level progression with increasing speed | Should | <br>
| F10 | Bonus fruit | Should | <br>
| F11 | Sound effects via PWM audio output | Could | <br>
| F12 | High score retained across games (until power-off) | Could | <br>

Non-functional: <br>
| N1 | Output 1280×720 @ 60 Hz VGA (74.25 MHz pixel clock) | Monitor reports correct mode | <br>
| N2 | 448×576 playfield (16×16 tiles, 32×32 sprites) centred in the frame | Visual check / frame dump | <br>
| N3 | 12-bit colour (RGB444) | Design review | <br>
| N4 | Input-to-screen latency under 100 ms | High-speed phone video of button press vs screen | <br>
| N5 | Game logic updates at 60 Hz, synchronised to vsync | Simulation | <br>
| N6 | Design meets timing in Vivado (no negative slack) | Timing report | <br>
| N7 | Fits in the Artix-7 35T; block RAM use under 50% | Utilisation report | <br>
| N8 | Total hardware cost under £150 | Bill of materials | <br>

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
