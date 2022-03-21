---
title: "Midterm 02 (Practice)"
date: 2022-03-20
type: book

summary: "The practice exam for midterm 02, EE260, spring, 2022."

tags:
- teaching
- ee260
- midterms

weight: 04
---

**Multiple Choices Questions (8 pts)**

1) (2 pts) Which of the following statements is true of testbench?
 - a. A testbench consists of one main element named a module.
 - b. A testbench provides a sequence of input values to test a module.
 - c. A testbench is a module with inputs and outputs.
 - d. A testbench creates an instance of a module named with the extension
   ''#tb''.

> - b.

2) (2 pts) The testbench for the given Verilog code snippet generates the waveform shown in the figure. Which of the following statements holds true in this case?
 - a. y_tb is set to 1 at 30 ns.
 - b. y_tb after 30 ns retains a value of 0 until y_tb is assigned a new value.
 - c. b_tb is set to 1 at 50 ns.
 - d. b_tb after 30 ns retains a value of 0 until b_tb is assigned a new value.

```
`timescale 1 ns/ 1 ns
module SetTimer (a, b, y);
   input a, b; 
   output reg y;


   always @ (a, b) begin
      y = a & b;
   end
endmodule


module Testbench ();
   reg a_tb, b_tb;
   wire y_tb;
   SetTimer SetTimer_tb (a_tb, b_tb, y_tb);
 
   Initial begin
      a_tb = 0;
      b_tb = 0;
      #20 b_tb = 1;
      #10 a_tb = 1;
      b_tb = 0;
      #10 a_tb = 0;
      #10 a_tb = 1;
    end
endmodule
```

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/problem_2.png" width=400 >}} |
| -- |

> - d.

3) (2 pts) The given FSM has input b, output z, and starts in state m. What is the FSM's resulting output and state if on the clock’s rising edge b is 0?
 - a. z = 0, state = m
 - b. z = 1, state = m
 - c. z = 0, state = n
 - d. z = 1, state = n

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/problem_3.png" width=300 >}} |
| -- |

> - c.

4) (2 pts) When implementing the FSM as a controller, how many outputs does the combinational logic block require?
 - a. 2
 - b. 3
 - c. 4
 - d. 6

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/problem_4.png" width=400 >}} |
| -- |

> - c.

**Short-Answer Questions (40 pts)**

1) (5 pts) Compare the behavior of D latch and D flip-flop devices by completing the timing diagram in Figure below. Provide a brief explanation of the behavior of each device. Assume each device initially stores a 0.

> | {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/solution_1.png" width=400 >}} |
> | -- |

2) (5 pts) A circuit has an input X that is connected to the input of a D flip-flop. Using additional D flip-flops, complete the circuit so that an output Y equals the output of X’s flip-flop but delayed by two clock cycles. 

> | {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/solution_2.png" width=400 >}} |
> | -- |

3) (5 pts) Draw a state diagram for an FSM with no inputs and three outputs x, y, and z. xyzshould always exhibit the following sequence: 000, 001, 010, 100, repeat. The output should change only on a rising clock edge. Make 000 the initial state.

> | {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/solution_4.png" width=400 >}} |
> | -- |

4) (5 pts) Using the process for designing a controller, convert the FSM you created for the previous problem to a controller, implementing the controller using a state register and logic gates.

> | {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/solution_5.png" width=400 >}} |
> | -- |

5) (5 pts) Trace the behavior of an 8-bit parallel load register with 8-bit input I, 8-bit output Q, load control input ld, and synchronous clear input clr by completing the timing diagram in Figure below.

> | {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/solution_6.png" width=400 >}} |
> | -- |

6) (5 pts) Draw the gate level design of a 1-bit full adder. Draw the schematic of a 8-bit carry-ripple adder using eight 1-bit full adders. Assuming AND gates have a delay of 2 ns, OR gates have a delay of 1 ns, and XOR gates have a delay of 3 ns, compute the longest time required to add two numbers using an 8-bit carry-ripple adder.

> | {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/solution_7a.png" width=400 >}} |
> | -- |

> | {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/solution_7b.png" width=400 >}} |
> | -- |

> From the illustration above, we see that both the FA and HA have a maximum gate delay of 3 ns. Therefore, 8 adders * 3 ns/adder = 24 ns is required for an 8-bit carryripple adder to ensure a correct sum is on the adder’s output. 

> An answer of 23 ns is also acceptable since the carry out of a half-adder will be correct after 2 ns, not 3 ns, and a half-adder may be used for adding the first pair of bits (least significant bits) if the 8-bit adder has no carry-in.

7) (5 pts) Use magnitude comparators and logic to design a circuit that computes the minimum of three 8-bit numbers.

> | {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/solution_8.png" width=400 >}} |
> | -- |

8) (5 pts) You are asked to design a comparator for three-bit 2’s complement numbers. A[0:2] and B[0:2] are both 2’s complement numbers with A2 and B2 being the MSBs. If A < B then LT should be 1 and the other outputs 0. If A > B then GT should be 1 and every other output 0. If A=B then EQ should be 1 and every other output 0.  

- a.	List the following 3-bit 2’s complement numbers in order from smallest to largest: 111, 101, 011, 010, 100.
- b.	Write the logic equations for LT, EQ and GT. Be sure to circle your final answer. Be sure you have also circled any intermediate values (nodes) you are using in your final answer.


> | {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/miterm_02_practice/images/problem_9.png" width=400 >}} |
> | -- |

> - a. 100(-4), 101(-3), 111(-1), 010(2), 011(3)
> - b. <a href="https://www.codecogs.com/eqnedit.php?latex=EQ&space;=&space;(\bar{A_2}&space;\oplus&space;B_2)\cdot&space;(\bar{A_1}&space;\oplus&space;B_1)\cdot&space;(\bar{A_0}&space;\oplus&space;B_0)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?EQ&space;=&space;(\bar{A_2}&space;\oplus&space;B_2)\cdot&space;(\bar{A_1}&space;\oplus&space;B_1)\cdot&space;(\bar{A_0}&space;\oplus&space;B_0)" title="EQ = (\bar{A_2} \oplus B_2)\cdot (\bar{A_1} \oplus B_1)\cdot (\bar{A_0} \oplus B_0)" /></a>  
> - c. <a href="https://www.codecogs.com/eqnedit.php?latex=GT&space;=&space;(\bar{A_2}&space;\cdot&space;B_2)&space;&plus;&space;(\bar{A_2}&space;\oplus&space;B_2)&space;\cdot&space;(A_1&space;\cdot&space;\bar{B_1})&space;&plus;&space;(\bar{A_2}\oplus&space;B_2)&space;\cdot&space;(\bar{A_1}&space;\oplus&space;B_1)&space;\cdot&space;(A_0&space;\cdot&space;\bar{B_0})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?GT&space;=&space;(\bar{A_2}&space;\cdot&space;B_2)&space;&plus;&space;(\bar{A_2}&space;\oplus&space;B_2)&space;\cdot&space;(A_1&space;\cdot&space;\bar{B_1})&space;&plus;&space;(\bar{A_2}\oplus&space;B_2)&space;\cdot&space;(\bar{A_1}&space;\oplus&space;B_1)&space;\cdot&space;(A_0&space;\cdot&space;\bar{B_0})" title="LT(\text{mirror of GT}) = (\bar{A_2} \cdot B_2) + (\bar{A_2} \oplus B_2) \cdot (A_1 \cdot \bar{B_1}) + (\bar{A_2}\oplus B_2) \cdot (\bar{A_1} \oplus B_1) \cdot (A_0 \cdot \bar{B_0})" /></a>  
> - d. <a href="https://www.codecogs.com/eqnedit.php?latex=LT&space;=&space;(\bar{EQ}&space;\cdot&space;\bar{GT})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?LT&space;=&space;(\bar{EQ}&space;\cdot&space;\bar{GT})" title="GT(\text{mirror of LT}) = (\bar{EQ} \cdot \bar{GT})" /></a>  

