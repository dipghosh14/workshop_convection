# workshop_convection

To get the tutorial files, open a terminal (ctrl+alt+t or click on the terminal button), then:

    git clone https://github.com/dipghosh14/workshop_convection.git

This creates a folder workshop_convection in your home directory.
**Running ASPECT**

To run a simulation:

    cd ~/workshop_convection/
    ~/aspect/aspect workshop.prm

Interesting files to look at:

- output/log.txt - use xdg-open or leafpad
- output/statistcs - same or plot using gnuplot, see below
- output/solution.pvd - open in ParaView

**How to plot statistics**

    cd ~/aspect-tutorials/
    gnuplot
    plot "output/statistics" using 2:20 with lines

This plots the surface heat flux (column 20) over the time (column 2)

**How to run in parallel**

    mpirun -np 2 ~/aspect/aspect tutorial.prm

