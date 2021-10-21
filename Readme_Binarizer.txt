Single Molecule Trajectory Binarizer Readme File
Authors: Connor Thomas, Srijit Mukherjee
JILA-NIST/CU Boulder, CO-80309
Matlab Live Script Version Info: Matlab R2021 with fit toolbox
%----------------------------------------------%

File Name: LoopedBin_5.mlx 
Input Data format: time trace tarjectories *.csv format. (col (1): frame/time col (2,:): fluorescence intensity info)

%----------------------------------------------% 
Description: This code accepts noisy single-molecule fluorescence time traces and tries to binarize them based on an input guess "on" value. The code binarizes the on and off time traces, provides information on the statistics of on and off events, fits the binned on and off data to a biexponential decay to give a time constant based on a Possionian distribution.
%----------------------------------------------%
# Section 1: Choose upto 8 fluorescence traces to track the frame/time information with fluorescence intensity 
* Select upto 5 traces with a "guess value" for a single molecule on event. 
* Note this is a guess "on" only - program will go through re-iterative protocols to polish this value
* Run this section only.

# Section 2: Defines selected "On" time and displays it and associated stats
* Set the trace number (upto 5) for the 1D array "ChosenOne" and "BlinksStart" and "BlinksEnd" to define the guess "on" time values
* Check on the plot in section 2 to see if the mean and standard deviations reported for the guess "on" make sense for the trace. (ex: is the off-event included in standard deviation window of the mean guessed on)
* If not: re-define the guess "on" 
* If yes: Run the rest of the code.

# Section 3: Extracts noise of dataset and fits it to a random distribution.

# Section 4: Identifies state changes and binarizes based on them.

# Section 5: Binarized trace storage

Section 6: 
* Fits on and off times to mono or  biexpoential fits and reports relevant stats
* If fits are not converging, starting values can be changed