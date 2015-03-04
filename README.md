# SWItest
Series IPython notebooks with test cases for the SWI package in MODFLOW 2005

The gridObj used in some of the scripts can by found in the SWItest/master/utils folder

## SWI 1D model
A single confined layer. GHB on the LHS representing an ocean bcn. WEL on the 
RHS representing the freshwater coming from land.
One stress period is defined of perlen days and is devided into nstp time steps 
and only the solution at the end of the stress period is written as output.
http://nbviewer.ipython.org/github/bdestombe/SWItest/blob/master/SWI1D/run1.ipynb

### Front reaches bottom of the aquifer
The flow is increased such, that the 50% front reaches the bottom of the confined aquifer. From this point, the SWI solution is only defined within the aquifer and therefore remains at the bottom of the aquifer.
http://nbviewer.ipython.org/github/bdestombe/SWItest/blob/master/SWI1D/reachBot.ipynb

### Not in steady state
The stress period is decreased by a factor of 250, now the model is not approaching steady state just yet, therefore the SWI solution and the Badon Ghyben Herzberg cannot be compared. We will do this anyway.
http://nbviewer.ipython.org/github/bdestombe/SWItest/blob/master/SWI1D/notSteady.ipynb

### Inclined downwards, confined
This version describes an inclined confined aquifer. Watch out! Large parts of the cells stand dry!
The SWI solution behaves like it should and doesnt crawl upward
http://nbviewer.ipython.org/github/bdestombe/SWItest/blob/master/SWI1D/inclined1conf.ipynb

### Inclined upwards, confined
This version describes an inclined confined aquifer in the opposite direction. There is no interface, everything is salt. isource is 0 for the well, so saline water is entering from the RHS.
http://nbviewer.ipython.org/github/bdestombe/SWItest/blob/master/SWI1D/inclined2conf.ipynb

### Inclined thin aquifer, zini
This version shows an confined aquifer, freshwater heads are around 0m. The initial zeta surface is placed a little bit above the bottom of the single aquifer. The interface is at steady state (tscale 100 changed to 1000 gave no difference). The interface is not able to move upwards, but (with playing with zini) the interface does move down if placed above the BGH solution.
http://nbviewer.ipython.org/github/bdestombe/SWItest/blob/master/SWI1D/inclined1conf_thin.ipynb
