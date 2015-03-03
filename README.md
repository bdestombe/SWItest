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
