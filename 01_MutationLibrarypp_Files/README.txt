AMRI'S Note:

These files are located in COOLFluiD/plugins/Mutationpp/

Adding the lookup table** to interpolate the following thermodynamic variables
(instead of computing them at each iteration): 

a: sound speed
h: enthalpy
e: energy
d: density 



The thermodynamic variables depend only of the temperature and the pressure because
of the Local thermodynamic equilibrium assumption.
** Look up table: 
For an array of pressure P=[P1 P2 .... Pn] and Temperature T = [T1 T2 ... Tk]
1) Computation AT ONCE of : 
	- a(Pi,Tj) 
	- h(Pi,Tj)
	- e(Pi,Tj)
	- d(Pi,Tj)
   stocked in a table. 

2) From the given set (P,T) at each iteration, the previous variable are not computed 
   but interpolated from the table build in step 1. 