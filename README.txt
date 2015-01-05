The Game of Life Simulator in MIPS
By Nicholas Colclasure

Currently, the simulator is controlled by 5 globals declared in the .data section.
set_grid_x sets the width of the field.
set_grid_y sets the height of the field.
set_iterations sets the number of iterations.

on_state_char sets the character representing on, and
off_state_char sets the character representing off.
Currently off_state_char does nothing, while on_state char
is used when reading a file representing a state of the grid.

default_file_ptr is the path of the file to use as the initial
state for the simulator. Currently, reading the state works by
looking at each character of the file, and if it is equal to
on_state_char the corresponding part of the grid is set to 1.
Otherwise that part is set to 0. This ignores newlines and
treats the specification as a sequential listing of the states,
starting at (0,0) and moving from left to right, then downward
one line at a time.