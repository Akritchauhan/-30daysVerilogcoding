# IMPLEMENTATION OF BASIC GATES

// VERILOG CODE
module gates (
  input a, b,
  output y_and, y_or, y_xor, y_not_a, y_xnor
);

  and  (y_and,   a, b);   
  or   (y_or,    a, b);  
  xor  (y_xor,   a, b);
  not  (y_not_a, a);      
  xnor (y_xnor,  a, b);   

endmodule

//TESTBENCH CODE
module testbench();
  reg a, b;
  wire y_and, y_or, y_xor, y_not_a, y_xnor;

  gates tb(a, b, y_and, y_or, y_xor, y_not_a, y_xnor);

  initial begin
    $dumpfile("dump.vcd");
    $dumpvars(0, testbench);

    $monitor("Time=%0t | a=%b, b=%b => AND=%b, OR=%b, XOR=%b, NOT a=%b, XNOR=%b", 
              $time, a, b, y_and, y_or, y_xor, y_not_a, y_xnor);

    a = 0; b = 0;
    #10 a = 0; b = 1;
    #10 a = 1; b = 0;
    #10 a = 1; b = 1;
    #10 $finish;
  end
endmodule

