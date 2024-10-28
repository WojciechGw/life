based on
https://github.com/grakoczy/picocomputer-game-of-life/tree/main</br>
by grakoczy

for Picocomputer 6502 designed by Rumbledethumps</br>
[Picocomputer GitHub](https://github.com/picocomputer)

# John Conway's Game of Life for Picocomputer 6502

is a cellular automaton that is played on a 2D square grid.

Each square (or 'cell') on the grid can be either alive or dead,
and they evolve according to the following rules:
1. Any live cell with fewer than two live neighbours dies (referred to as underpopulation).
2. Any live cell with more than three live neighbours dies (referred to as overpopulation).
3. Any live cell with two or three live neighbours lives, unchanged, to the next generation.
4. Any dead cell with exactly three live neighbours comes to life.
The initial configuration of cells can be created by a human, but all generations thereafter
are completely determined by the above rules.
The goal of the game is to find patterns that evolve in interesting ways - something
that people have now been doing for over 50 years

source of text above https://conwaylife.com/

# RP6502 VSCode for LLVM-MOS

### LLVM PATH notes

LLVM-MOS must be in your PATH. However, this may conflict with other LLVM
installations, like the one that comes with your operating system.
In that case, you can adjust the path for only CMake with a VSCode setting.
Add a file `.vscode/settings.json` with the following contents. Adjust the
path for where you installed LLVM-MOS.
```
{
    "cmake.environment": {
        "PATH": "~/llvm-mos/bin:${env:PATH}"
    }
}
```
