# TITTLE
Implement AND gate using nor gate only
# THEORY
```
We can derive the equivalent NOR gate circuit for an AND gate using De Morgan's theorem.

The expression for the output of the AND gate is:

Output = A AND B

Using De Morgan's theorem, we can rewrite this as:

Output = NOT(NOT(A) OR NOT(B))


In this circuit:

NOR1 takes the inputs A and B and gives the NOR of A and B as output.
NOR2 takes the output of NOR1 and gives the NOR of NOR1's output and NOR1's output as output.
NOR3 takes the output of NOR2 and gives the NOR of NOR2's output and NOR2's output as the final output.
The output of NOR3 is equivalent to the output of an AND gate with inputs A and B.
```


# NETLIST DIAGRAM
![image](https://github.com/KotiSaiSankar/Simulation-project--Digital-Electronics/assets/118344248/d9c595bf-7bbb-4d91-a4fe-68f4c61fcf78)



# TIMING DIAGRAM
![image](https://github.com/KotiSaiSankar/Simulation-project--Digital-Electronics/assets/118344248/80be0905-a6af-44ab-9655-4c3a547d38e8)


# PROGRAM
```
module ccc(x,y,z,u,v,w,f,g);
input x,y,z,u,v,w;
output f,g;
wire a,b,c;
nor (a,x,y,z);
nor (b,u,v,w);
nor (g,a,b);
nor (f,g);
endmodule
```

# REFERENCE

