# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

/* write all the steps invloved */

**PROGRAM**<br>
module exp9(T,clk,Q,Qbar);<br>
input T,clk;<br>
output reg Q;<br>
output reg Qbar;<br>
initial Q=0;<br>
initial Qbar=1;<br>
always @(posedge clk)<br>
begin<br> 
Q=(T&(~Q))|((~T)&Q);<br>
Qbar=~Q;<br>
end<br>
endmodule<br>

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL LOGIC FOR FLIPFLOPS**<br>
![390978992-d38b4675-c9ee-4ea5-b780-9761dc1f6aa7](https://github.com/user-attachments/assets/0d711046-33ae-493e-8302-75ace5c7016d)


**TIMING DIGRAMS FOR FLIP FLOPS**<br>
![390979025-37a3cdff-6dfe-43dd-abee-3622a8bc0179](https://github.com/user-attachments/assets/9237a384-ccf0-4b57-8791-02ec6cc2db54)


**RESULTS**<br>
To implement T flipflop using verilog and validating their functionality using their functional tables are verified.
