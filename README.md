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
```
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: ISTIN B
RegisterNumber:212223040068
```
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
![Screenshot (179)](https://github.com/user-attachments/assets/f4386c97-d12e-401b-afb2-8fb3cf7f4830)


## Truth table
![image](https://github.com/23004205/BOOLEAN_FUNCTION_MINIMIZATION/assets/138971114/a9ccb75e-db7b-490e-8b69-10f820e6bff4)


![image](https://github.com/23004205/BOOLEAN_FUNCTION_MINIMIZATION/assets/138971114/6835b6c0-9fe5-4f55-8288-53b7d0c42104)
## Timing Diagram
![ex2o](https://github.com/user-attachments/assets/197bcc56-fe7d-42df-bbe6-e0521f0d13b9)



## Result:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

