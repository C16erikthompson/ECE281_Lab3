ECE281_Lab3
===========

#Moore Basic Functionality

Getting the Moore elevator to work was deceptively easy, only needing to instantiate the Moore CE3 shell to get it to work

#Mealy Basic Functionality

Getting the Mealy elevator to function was identical to the Moore functionality, only requiring that I add another nibble output for next floor

# More Floors

Implementing more floors required altering the implemented CE3 shell to include 4 additional floors.  Just as well, an additional output needed to
be created to account for prime numbers that exceeded the ones space (i.e. 11, 13, 17, & 19).  To make the Nexys output the prime numbers, the output
values were changed for CE3

# Change Inputs

To implement change inputs, the Moore CE3 outputs were changed to reflect floors 0-7.  In addition to that, the inputs for the CE3 needed to be changed,
having a std_logic_vector as an input, while changing the up_down and stop inputs into signals activated by if statements, triggered by the floor inputs

#Moving Lights

To implement moving lights, I had to figure out how exactly the lights worked.  Unable to get a very clear idea of how they moved, I tried several different
things, eventually getting it to work by reversing the order of that the lights occur, by placing them in a process in the nexys top shell.
Which order of lights is happening and if the lights are on was determined by an outputs from CE3, that are either high or low based upon a set of circumstances.
