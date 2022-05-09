---
draft: false
title: "Final Exam"
date: 2022-05-09
type: book
commentable: true

summary: "The final exam, EE260, spring, 2022."

tags:
- teaching
- ee260
- final

weight: 08
---

**Multiple Choices Questions (20 pts)**

1) (2 pts) Which of the following is a sum-of-minterm representation of a(b + c')?
 - a. ab + ac'
 - b. abc + abc' + ab'c'
 - c. abc + abc' + ab'c' + a'bc'
 - d. abc + abc' + a'bc'


2) (2 pts) A two-input XNOR gate is equivalent to which equation?
 - a. y = ab'
 - b. y = ab' + a'b
 - c. y = a(b' + b)
 - d. y = a'b' + ab

3) (2 pts) What does the following circuit output?

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_game/images/multi_problem_3.png" width=300 >}} |
| -- |

 - a. 00000000
 - b. 00000100
 - c. 10100000
 - d. 111110111

4) (2 pts) How many bits does the state register of an FSM with 7 states require?
 - a. 1
 - b. 2
 - c. 3
 - d. 4

5) (2 pts) An FSM's initial state s is encoded as 000, so the FSM's circuitry sets the state register's clear input to 1 for a few microseconds upon startup. Which is a typical method?
 - a. The initial state should have the action "clear = 1".
 - b. The initial state should have the action "clear = 0".
 - c. The initial state should have a transition back to itself.
 - d. Special circuitry sets the register's clear signal to 1 upon startup.

6) (2 pts) Consider a barrel shifter with eight shift control inputs. How many 1-bit shifters are required to design the mentioned barrel shifter?

 - a. Eight 1-bit barrel shifters
 - b. Sixteen 1-bit barrel shifters
 - c. Sixty-four 1-bit barrel shifters
 - d. Two hundred fifty-six 1-bit barrel shifters

7) (2 pts) Eight 1 KB memory chips (10 address inputs) named C0, C1, ..., C7 (top to bottom) are composed into an 8 KB memory (13 address inputs). Which of the following sentences is true in this case.

 - a. For address 1010000000111, chip C7 is activated
 - b. For address 0110110000000, chip C0 is activated
 - c. For address 1010000000111, chip C5 is activated
 - d. For address 0110110000011, chip C2 is activated

8) (2 pts) The HLSM describes the loop behavior of a pulse generator. The output z is connected to the bulb and the pulse generated switches on the bulb. For how many clock cycles is z set to 1?

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_game/images/multi_problem_8.png" width=500 >}} |
| -- |

 - a. 2 clock cycles
 - b. 4 clock cycles
 - c. 8 clock cycles
 - d. 16 clock cycles

9) (2 pts) For the given diagram, identify the action in ON state.?

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_game/images/multi_problem_9.png" width=500 >}} |
| -- |

 - a. B_s = 0 and B_ld = 1
 - b. B_s = 0 and B_ld = 0
 - c. B_s = 1 and B_ld = 0
 - d. B_s = 1 and B_ld = 1

10) (2 pts) Identify XXX in the Verilog code snippet that uses the correct logical operator for the given FSM?

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_game/images/multi_problem_7.png" width=500 >}} |
| -- |

```
I_Init: begin
   XXX
      I_State = I_Count;
   end
...
end

```

 - a. ``` if (a') begin ```
 - b. ``` if (!a) begin ```
 - c. ``` if (~a) begin ```
 - d. ``` if (not a) begin ```

**Short-Answer Questions (80 pts)**

1) (10 pts) Design a 4-1 multiplexer using only NOR gate. Show the truth table and logic circuit.

 |  |
 |--|

2) (10 pts) Using only T flip-flops and standard gates, design a device which divides a clock by 8 and has a duty cycle of 1/8th.

 |  |
 |--|

3) (10 pts) Say you are working in a system where the only component you have available is a 2-to-1 MUX. Show how to build a 2-input NOR gate from those MUXes. You can freely connect inputs to "1" and "0" as needed. Label the inputs as "A" and "B". Label the output as "X". Your solution must use 3 or fewer of the MUXes to receive credit.

 |  |
 |--|

4) (10 pts) Design a finite state machine (FSM) for a counter that counts through the 3-bit prime numbers downwards. Assume the counter starts with initial prime value set to 010 as its first 3 bit prime number. You need to provide the state transition table and the state transition diagram. Assume that the state is stored in three D-FFs. Hint: The set of all 3-bit prime numbers includes 2, 3, 5 and7.

 |  |
 |--|

5) (10 pts) Write the finite state machine (FSM) of the circuit shown below. Hint: In the given DEMUX below, S2 is the input signal, S1=Q1, S0=Q0, and there is a single output labeled as M. 

| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_game/images/short_problem_5.png" width=500 >}} |
 |--|

6) (10 pts) Use a Karnaugh map to find all of the static hazards in the corresponding two-level circuit, and design a hazard-free circuit that realizes the same logic functions: F = W'X' + Y'Z + W'XYZ + WXYZ'
 (The definition of static hazards can be found here: https://en.wikipedia.org/wiki/Hazard_(logic)#Static_hazards)

 |  |
 |--|

7) (10 pts) Consider flip-flops A, B and C each nominally clocked off of the same clock. Assume:
 - a. Each flip-flop has a set-up time of 5ns and a clock-to-Q delay of 3ns to 4ns,
 - b. The AND and OR gates each have a delay of 2 to 6 ns,
 - c. The NOT gate has a delay of 1 to 5 ns.

  Answer the following questions and show your work:
 - Q1. What is the shortest clock period you could safely clock this system at? Show your work. 
 - Q2. What is the (non-negative) range of values for the flip-flop’s hold time would be sufficient?


| {{< figure src="https://raw.githubusercontent.com/gustybear-teaching/course_ee260_2022_spring/main/final_game/images/short_problem_8.png" width=500 >}} |
| -- |

8) (10 pts) You wish to design a state machine that has one input "A" and one Moore-type output "Z". Z should be a 1 if and only if the last 6 values of A were "0". Due to budget cuts, you only have the following devices available:

 - a. 2-input gates of any standard type (AND, OR, NOR, NAND, XOR, and XNOR).
 - b. Inverters
 - c. Modulo-16 counters with enable and reset
 - d. 4 to 16 decoders 
 - e. 2-to-1 MUX (1-bit wide).

   Using as few devices as possible, implement the state machine described above. Solutions which use more than 4 devices will receive no credit.
