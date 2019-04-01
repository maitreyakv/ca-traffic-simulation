-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
||                 CATS - CELLULAR AUTOMATA TRAFFIC SIMULATION               ||
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

Author          : Maitreya Venkataswamy
Created         : April 1, 2019
Last Modified   : April 1, 2019

Affiliation          : Georgia Institute of Technology

Contents:
1. SOFTWARE DESCRIPTION
2. INSTALLATION - RELEASE
3. INSTALLATION - DEBUG
4. EXECUTION

-------------------------------------------------------------------------------
                        1. SOFTWARE DESCRIPTION
-------------------------------------------------------------------------------

This software uses cellular automata to simulate the movement of vehicles
through a two lane road. The software uses OpenMP for parallelization of the
simulation.

The software requires the GNU C compiler with OpenMP enabled.

-------------------------------------------------------------------------------
                        2. INSTALLATION - RELEASE
-------------------------------------------------------------------------------

To build the vortex simulation program, run the following commands

    $ cd cmake-build-release
    $ cmake .
    $ make

This will build the executable "cats".

-------------------------------------------------------------------------------
                        3. INSTALLATION - DEBUG
-------------------------------------------------------------------------------

To build the vortex simulation program in debug mode, run the following
commands

    $ cd cmake-build-debug
    $ cmake .
    $ make

This will build the executable "cats" in debug mode. The debug mode makes the
following modifications to the program:

    1. The random number generator is seeded with a constant, so that the
        the results are reproducible.
    2. The number of threads is locked to 1
    3. Print statements are included in many parts of the code to assist in the
        debugging process. These include simple visualizations of the road at
        each step in the simulation.

-------------------------------------------------------------------------------
                            4. EXECUTION
-------------------------------------------------------------------------------

To run the simulation program, copy the executable file "cats" into a directory
where you want to run the simulation. A configuration file "cate-input.txt"
needs to be placed alongside the executable. A sample configuration file is
included in both of the build folders where the executable was created.

    $ ./cats <nthread>

where <nthread> is the number of threads that you want to run the program with.