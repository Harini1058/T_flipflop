# T_flipflop
# AIM:

To implement T flipflop using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:

Quartus prime

# THEORY

T Flip-Flop

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

<img width="541" height="363" alt="Screenshot 2025-12-15 191120" src="https://github.com/user-attachments/assets/b08be70d-3255-4182-a1ad-8898ae615f6d" />


This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

<img width="454" height="344" alt="Screenshot 2025-12-15 191135" src="https://github.com/user-attachments/assets/7bc4b243-b868-434a-ae02-aba3f5955e3e" />


From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

# Procedure

Type the program in quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

# PROGRAM

# Developed by : HARINI G
# Register number : 25015377

module t_ff (
    input  wire clk, rst, T,
    output reg Q 	  
);

  initial begin
     Q<=1'b0;
	 end
  
  
	 always @(posedge clk or posedge rst) begin
	
        if (rst)
            Q <= 1'b0;       // Reset
        else if (T)
            Q <= ~Q;         // Toggle if T=1
        else
            Q <= Q;          // Hold if T=0
    end
endmodule

# RTL LOGIC FOR FLIPFLOP

<img width="1325" height="788" alt="Screenshot 2025-12-15 111618" src="https://github.com/user-attachments/assets/e4c6614e-3bb4-4c69-b31c-4750ca43b1b2" />

# TIMING DIGRAMS FOR FLIP FLOPS

<img width="1819" height="951" alt="Screenshot 2025-12-15 134913" src="https://github.com/user-attachments/assets/f83ee069-c990-4974-a04c-bede11133c1d" />

# RESULTS

Thus T flipflop using verilog has implemented and validating their functionality using their functional tables have completed successfully.
