# TITTLE
###Design and simulate octal to binary encoder using Verilog.
# THEORY
In this example, the OctalToBinaryEncoder module takes a 3-bit octal input (octal) and converts it to an 8-bit binary output (binary). It uses a combinational case statement to map each octal input value to the corresponding binary output value. The default case is used to handle any unexpected input and set the binary output to zero.

To simulate this module, you can use any Verilog simulator. Here's an example testbench to demonstrate the functionality:
# LOGIC DIAGRAM
![image](https://github.com/mathanrajsaveetha/Simulation-project--Digital-Electronics/assets/119560501/e872d4da-9ab6-4187-8a27-7d7f3aeb94bf)

# NETLIST DIAGRAM

# TIMING DIAGRAM
![image](https://github.com/mathanrajsaveetha/Simulation-project--Digital-Electronics/assets/119560501/f84dec68-4f30-43e8-97f5-65bec49fcb16)

# PROGRAM\
```
module OctalToBinaryEncoder (
  input [2:0] octal,
  output reg [7:0] binary
);

  always @(octal) begin
    case (octal)
      3'b000: binary = 8'b00000001;
      3'b001: binary = 8'b00000010;
      3'b010: binary = 8'b00000100;
      3'b011: binary = 8'b00001000;
      3'b100: binary = 8'b00010000;
      3'b101: binary = 8'b00100000;
      3'b110: binary = 8'b01000000;
      3'b111: binary = 8'b10000000;
      default: binary = 8'b00000000;
    endcase
  end

endmodule
```
# REFERENCE
