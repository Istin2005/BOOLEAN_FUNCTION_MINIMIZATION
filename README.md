# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: ISTIN B
RegisterNumber:212223040068
```
module Boolean_min(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);

and(s,x,y);
and(t,w,y);
and(u,ydash,z);
or(f2,s,t,u);
endmodule
```



## RTL realization
![Screenshot (19)](https://github.com/SanjayK2006/BOOLEAN_FUNCTION_MINIMIZATION/assets/144979178/ef48fcfa-6d2b-4c00-b704-2e1fc4d56af4)

## Truth table
![316294144-348e89c8-b4d6-4c9e-8783-541ac0829105](https://github.com/aaron-h-2k5/BOOLEAN_FUNCTION_MINIMIZATION/assets/144250957/89a5b37e-718b-44ec-806f-153c2772eca4)
## Timing Diagram
![Screenshot 2024-03-13 161036](https://github.com/04Varsha/BOOLEAN_FUNCTION_MINIMIZATION/assets/149035374/533d1307-308c-4a6d-9495-b6f289bf8479)

## Result:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

