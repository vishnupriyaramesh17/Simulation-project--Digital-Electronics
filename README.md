# TITLE
Design and generate 8 bit parity generator using Verilog.

# EQUIPMENTS REQUIRED

  Hardware – PCs, Cyclone II , USB flasher
  
  Software – Quartus prime

# THEORY

## Parity Generator
An 8-bit parity generator is a digital circuit that generates a parity bit based on a set of 8 input data bits. The purpose of the parity bit is to provide error detection in data transmission or storage systems.The parity bit is calculated based on the number of 1s in the input data bits. There are two types of parity: even parity and odd parity.In even parity, the parity bit is set to 1 if the number of 1s in the input data is odd. This ensures that the total number of 1s, including the parity bit, is always even.In odd parity, the parity bit is set to 1 if the number of 1s in the input data is even. This ensures that the total number of 1s, including the parity bit, is always odd.

## TRUTH TABLE

![8 bit tt](https://github.com/vishnupriyaramesh17/Simulation-project--Digital-Electronics/assets/119393589/0f29db89-aa61-4602-b853-b4f4567a0456)

# LOGIC DIAGRAM
![8 bit logic](https://github.com/vishnupriyaramesh17/Simulation-project--Digital-Electronics/assets/119393589/7c85313e-321c-40d3-9e24-e33d5fd67ba7)


# NETLIST DIAGRAM
![8 bit netlist](https://github.com/vishnupriyaramesh17/Simulation-project--Digital-Electronics/assets/119393589/c56ab7b7-a4a5-4d8a-a3d5-23981579e760)


# TIMING DIAGRAM

![timing 8 bit](https://github.com/vishnupriyaramesh17/Simulation-project--Digital-Electronics/assets/119393589/530c5a37-87b0-44c7-8451-8f9f791ebde3)


# PROGRAM
     Program to simulate 8 bit parity generator using Verilog.
     NAME : VISHNUPRIYA R
     REG.NO : 212222110054


     module parity_generator (
           input [7:0] data_in,
           output reg parity_out
       );

  

       always @(*) 
            begin
               reg [7:0] xor_result;
	  
              xor_result = data_in[0] ^ data_in[1] ^ data_in[2] ^ data_in[3] ^ data_in[4] ^ data_in[5] ^ data_in[6] ^ data_in[7];
	           parity_out= ~xor_result;
                 end

        endmodule

  

# REFERENCE
https://www.engineersgarage.com/vhdl-tutorial-12-designing-an-8-bit-parity-generator-and-checker-circuits/

https://www.electronicshub.org/parity-generator-and-parity-check/

https://codestall.wordpress.com/2017/09/04/parity-generator-in-verilog/

