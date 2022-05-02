---
title: "Final Exam (Practice)"
date: 2022-05-01
type: book
commentable: true

summary: "The practice exam for final, EE260, spring, 2022."

tags:
- teaching
- ee260
- final

weight: 07
---

**Multiple Choices Questions (20 pts)**

1) (2 pts) (a + a') b = (1)b = b uses which two Boolean algebra properties?
 - a. Associative, Commutative
 - b. Complement (OR), Identity (AND)
 - c. Commutative, Identity (AND)
 - d. Complement (AND), Identity (OR)


2) (2 pts) A 4x1mux is captured by which equation?

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/multi_problem_2.png" width=200 >}} |
| -- |

 - a. y = s0'i0 + s0i1 + s1'i2 + s1'i3
 - b. y = s1's0'i0 + s1's0i1 + s1s0'i2 + s1s0i3
 - c. y = (s1 + s0)(i3i2i1i0)
 - d. y = i3 + i2 + i1 + i0

3) (2 pts) A 2-bit register has data inputs d1, d0, clock input clk, and outputs q1, q0. Data inputs d1d0 is 01 and output q1q0 is 00. What does q1q0 become after the clk rises?
 - a. 00
 - b. 01
 - c. 10
 - d. 11

4) (2 pts) Which states are equivalent?

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/multi_problem_4.png" width=400 >}} |
| -- |

 - a. s, v
 - b. u, v
 - c. t, v
 - d. t, u

5) (2 pts) What is the equation for n0?

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/multi_problem_5.png" width=400 >}} |
| -- |

 - a. p1'p0' + p1p0
 - b. p1p0' + p0’b’ + p1p0
 - c. p0b + p1p0
 - d. p0’b’ + p1p0

6) (2 pts) Determine the number of transistors used to compute all partial products for the given 3-bit multiplier if a2a1a0 = 101 and b2b1b0 = 011.

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/multi_problem_6.png" width=300 >}} |
| -- |

 - a. 36 transistors
 - b. 3 transistors
 - c. 9 transistors
 - d. 63 transistors

7) (2 pts) A 4-bit adder/subtractor has inputs A = 0100, and B = 0010. What value of sub outputs sum S = 0110 and cout = 0000?

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/multi_problem_7.png" width=400 >}} |
| -- |

 - a. 0
 - b. 1
 - c. 0000
 - d. 1111

8) (2 pts) Which of the following results in the best simplification? Note: Each circle is denoted by parenthesis. (A, B) indicates that a circle includes cells A and B.

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/multi_problem_8.png" width=300 >}} |
| -- |

 - a. (m0, m1), (m3, m2), (m5, m7)
 - b. (m0, m2), (m1, m3, m5, m7)
 - c. (m0, m1, m3, m2), (m5, m7)
 - d. (m0, m1, m3, m2), (m1, m3, m5, m7)

9) (2 pts) Which of the following statements explains the difference between SRAM and DRAM?

 - a. SRAM is typically used for on-chip cache, DRAM is typically used for larger off-chip main memory
 - b. SRAM is slower than DRAM
 - c. SRAM is typically used for larger off-chip main memory, DRAM is typically used for on-chip cache
 - d. SRAM is denser and cheaper than a DRAM

10) (2 pts) Identify the Verilog description’s input and output declaration for the given HLSM.

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/multi_problem_9.png" width=400 >}} |
| -- |

 - a.
```
module ColorCoding_HLSM (clk, rst, a, B, Q); 
   input clk, rst;
   input a;
   input [9:0] B;
   output reg [9:0]Q;
 …
endmodule
```
 - b.
```
module ColorCoding_HLSM (clk, rst, a, B, Q); 
   input clk, rst;
   input a;
   input [0:9] B;
   output reg [0:9]Q;
…
endmodule
```
 - c.
```
 module ColorCoding_HLSM (Q, B, a, clk, rst); 
   input [10:0] B, a, clk, rst;
   output reg [10:0] Q;
…
endmodule
```
 - d.
```
module ColorCoding_HLSM (Q, B, a, clk, rst); 
   input [0:10] B, a, clk, rst;
   output reg [0:10] Q;
…
endmodule
```

**Short-Answer Questions (80 pts)**

1) (8 pts) Design a Full Adder using only one type of logic gate. Show the truth table and logic circuit.

 |  |
 |--|

2) (8 pts) A positive-edge-triggered J-K flip-flop has two control inputs J and K that control the device’s behavior at the rising edge of CLK. If only J is asserted, the Q output is set to 1; if only K is asserted, Q is clear to 0; if both are asserted, Q is toggled; and if neither is asserted, Q is not changed. Show how to build a J-K flip-flop using a D flip-flop and combinational logic.

 |  |
 |--|

3) (8 pts) Design a state transition diagram for a state machine which has one input "A" and one output "Z".  Z should go high if the most recent inputs were either "1001" or "010".  For full credit, you should use as few states as possible.

 |  |
 |--|

4) (8 pts) Analyze the state machine in the figure below. Write excitation equations, excitation transition table, and state/output table (use state A-H for Q1 Q2 Q3 = 000 – 111)

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/short_problem_3.png" width=500 >}} |
| -- |

5) (8 pts) Capture the following system behavior as an HLSM. The system has two single-bit inputs U and D each coming from a button, and a 16-bit output C, which is initially 0. For each press of U, the system increments C. For each press of D, the system decrements C. If both buttons are pressed, the system does not change C. The system does not roll over; it goes no higher than than the largest C and no lower than C=0. A press is detected as a change from 0 to 1; the duration of that 1 does not matter.

 |  |
 |--|

6) (8 pts) Consider the function F(a,b,c) = a’c + ac + a’b. Using a K-map: (a) Determine which of the following terms are implicants (but not necessarily prime implicants) of the equation: a’b’c’, a’b’, a’bc, a’c, c, bc, a’bc’, a’b. (b) Determine which of those terms are prime implicants of the function. (The definition of implicants and prime implicants can be found here: https://en.wikipedia.org/wiki/Implicant)

 |  |
 |--|

7) (8 pts) List the basic register/memory transfers and operations that occur during each clock cycle for the following program, based on the six-instruction instruction set of week 15, assuming that the content of D[9] is 0: 
```
        MOV R6, #1; 
        MOV R5, 9; 
        JMPZ R5, label1; 
        ADD R5, R5, R6; 
label1: ADD R5, R5, R6.
```
What is the value in R5 after the program completes? (show your work)

 |  |
 |--|

8) The code below should implement a simple four state FSM which increments a 4-bit synchronous counter when the FSM is in state 2'b10. Identify the major problem with this code when synthesized. Propose a solution to fix the problem. You can define a new variable if necessary

```
module simple_fsm(clk, reset, count);
  input reset, clk;
  output [3:0] count;
  reg [3:0] count;
  reg [1:0] state;
  reg [1:0] next;

  always @ (posedge clk) begin
    if (reset) state <= 2'b00;
    else state <= next;
  end

  always @ (state or reset or count) begin
    if (reset)
      count = 4'b0000;

    case (state)
      2'b00: next = 2'b01;
      2'b01: next = 2'b10;
      2'b10: begin
        next = 2'b11;
        count = count +1;
      end
      2'b11: next = 2'b00;
        default: next = 2’b00;
      endcase
  end
endmodule
```

9) (8 pts) Assume that the PC autoincrement time is 20ns, ALU propagation delay is 10ns for "pass A" ops (pass through whatever at the A to the output of the ALU) and 50ns for ADD, memory reads/writes are 50ns from stable addr, combinational logic delay is 10ns, register setup times are 10ns, and register propagation delays are 10ns 	

- a. Draw the control/data signals for MOV R7,R8 on the figure below, showing the timing as carefully as you can. Use X and Z to indicate unknown and high-impedance. Show the signal/data values right before the rising edge of the clock for this instruction if you can.
- b. How short could the clock period be (in ns) to execute this instruction? Why?
- c. If it were an ADD instead of a MOV, would it fit in 100ns? If so, how long would it take? If not, why not (and how long would it take)?
- d. If MOV R5, R6 is a single-cycle instruction, why is MOV R5, R0 a two-cycle instruction?

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/short_problem_9.png" width=400 >}} |
| -- |

10) (8 pts) On this page is a slightly modified data-path and state transition diagram for our shift-and-add multiplier. It doesn't quite work correctly. On the following page you will be asked some questions about it. 

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/short_problem_a.png" width=400 >}} |
| -- |

Fill in the following values. Use base-10 numbers. You are to assume that A=10112 and B=11012. Show all states up to and until "Waiting" is entered. If you can't determine a value, indicate that by writing an "X" in place of the value. 

Using only a few sentences, explain the simplest change(s) you can which would allow this multiplier to work correctly. This will be graded based on correctness, conciseness, simplicity and clarity of explanation.

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_practice/images/short_problem_a_1.png" width=400 >}} |
| -- |

