# BCD_7SEGMENT
# Aim:
To design and simulate BCD 7 Segment using vivado.

# Apparatus Required
PC with vivado software.

# Procedure
STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it.

STEP:5 Select the run simulation and then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 compare the output with truth table. image
![image](https://github.com/mattikuravasowmya/mattikuravasowmya/assets/161432676/b61c0e68-81fb-437a-91c8-041d0b6720f3)

# Program
//Verilog module. module segment7( bcd, seg );

 //Declare inputs,outputs and internal variables.
 input [3:0] bcd;
 output [6:0] seg;
 reg [6:0] seg;
//always block for converting bcd digit into 7 segment format

always @(bcd)

begin

    case (bcd) //case statement
    
        0 : seg = 7'b0000001;
        
        1 : seg = 7'b1001111;
        
        2 : seg = 7'b0010010;
        
        3 : seg = 7'b0000110;
        
        4 : seg = 7'b1001100;
        
        5 : seg = 7'b0100100;
        
        6 : seg = 7'b0100000;
        
        7 : seg = 7'b0001111;
        
        8 : seg = 7'b0000000;
        
        9 : seg = 7'b0000100;
        
        //switch off 7 segment character when the bcd digit is not a decimal number.
        
        default : seg = 7'b1111111; 
        
    endcase
    
end
endmodule

# Output:
![image](https://github.com/mattikuravasowmya/mattikuravasowmya/assets/161432676/7e639e20-b7a1-4dab-be4a-30f937d69053)
# Result:
Thus the BCD 7 Segment is verified succcessfully.



