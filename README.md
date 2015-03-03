# SWItest
Series IPython notebooks with test cases for the SWI package in MODFLOW 2005

The gridObj used in some of the scripts can by found in the SWItest/master/utils folder

## SWI 1D model
A single confined layer. GHB on the LHS representing an ocean bcn. WEL on the 
RHS representing the freshwater coming from land.
One stress period is defined of perlen days and is devided into nstp time steps 
and only the solution at the end of the stress period is written as output.
http://nbviewer.ipython.org/github/bdestombe/SWItest/blob/master/SWI1D/run1.ipynb
