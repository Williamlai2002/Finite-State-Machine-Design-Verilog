# Finite-State-Machine-Design-Verilog
implement a Finite State Machine (FSM) using one-hot encoding to recognize sequences of four consecutive 1s or 0s on the input signal w. The FSM outputs z = 1The FSM transitions through nine states, each represented by a single active flip-flop (y8, ..., y0) as per the one-hot encoding

<img width="324" alt="image" src="https://github.com/user-attachments/assets/3ae3cba1-7fd0-491b-a91c-e848deac9a32">


<img width="570" alt="image" src="https://github.com/user-attachments/assets/cc44d72f-444e-4f00-86ce-4dfbae2dff9e">

# Functionality
The FSM consists of 9 states, each represented by a dedicated flip-flop (y8 to y0) in a one-hot encoding scheme.
The FSM transitions between states based on the value of w, detecting:
Four consecutive 1s.
Four consecutive 0s.
The output z is set to 1 once a sequence is detected and remains 1 for overlapping sequences.
The system is designed to reset synchronously with an active-low reset signal.
Project Steps


# FSM Design:

Implement the FSM logic in sequence_detector_part_1.v using simple assign statements for the flip-flop inputs.
Derive state transition expressions from the one-hot encoding and state diagram.
I/O Assignments:

SW[0]: Active-low synchronous reset input.
SW[1]: Input signal w.
~KEY[0]: Clock input.
LEDR[8:0]: Displays the current state using 9 LEDs.
LEDR[9]: Displays the output z (sequence detected).

# How to Use
Modify the input (w) using SW[1].
Observe the FSM's current state on LEDR[8:0].
Check the output (z) on LEDR[9], which lights up when a sequence of four consecutive 1s or 0s is detected.
