Download Link: https://assignmentchef.com/product/solved-ece2220-lab1-quartus-ii-and-the-de10-standard
<br>
In this lab, using the Quartus II tutorial as a guide, you will learn the basics of using the Quartus® II software to create (using Verilog), simulate and implement a few very simple logic circuits on the DE10 standard board. Read and review the <em><u>Quartus Prime Introduction.</u>  </em>

<ol>

 <li>Create a new project and in a separate folder. The easiest way to do this is using the “New Project Wizard”. Save only one project in each folder. Choose “5CSXFC6D6F31C6” (about 6<sup>th</sup> from the bottom of the list) as the device in “Assign” menu.</li>

</ol>

<strong>NOTE: </strong>The name of the Verilog file must be the same as the name used for the top module. <strong> </strong>

<ol>

 <li>Create a new Verilog file (File-New-Verilog HDL). A new “Verilog” window will open.</li>

</ol>

Implement the following in Verilog

<ol>

 <li>Create two input signals “x” and “y”</li>

</ol>

<ol>

 <li>Using the structural formation, implement x <strong>AND </strong>y, x <strong>OR </strong>y, and x <strong>XOR </strong> Create (and show) a “Simulation Waveform Editor” File (New-University Program VWF) and a waveform window will open.

  <ol>

   <li>Create the waveforms for the inputs, x and y and run a “functional” simulation for the 3 logic functions.</li>

  </ol></li>

</ol>




<ol start="3">

 <li>Use the switches SW[0] and SW[1] as the inputs and the LEDR[0], LEDR[1], and LEDR[2] for the output of the three logic functions;  for  x <strong>AND </strong>y,  x <strong>OR </strong>y, and x <strong>XOR </strong> The pin assignments may be found either in the DE10 manual or in the DE10-Standard Pin Assignments file.  Compile the code and download it to the DE10 board. (You will need to follow the directions in Section 3.3 of the DE10 manual closely particularly the part to “Configure the FPGA in JTAG Mode”.</li>

</ol>

<strong><u>*Note:</u></strong> You will notice that the other LEDS seem to be on slightly. This is due to the fact that the default output is for a “weak” pull-up. The other LEDS can be turned off:  Go back to the top level design. Click the following; 1) “Assignments”, 2) “Device”, 3) “Pin and Device Options” and then 4) “Unused Pins”.  Change this setting to “As input tri-stated”.

<ol>

 <li>The following circuit is for a 1 bit full adder. Partial Verilog code for it is written in structural formation. The <strong>wire</strong> element used in the highlighted section of Verilog code is a keyword used to connect input and output ports of a module instantiation together with some other element in your design. Complete the code using similar logic as in the partially written code.</li>

</ol>

Use the switches SW[0], SW[1] and SW[2] as the inputs and the LEDR[0] and LEDR[1] for the outputs of sum and cout. Compile the code and download it to the DE10 board.

<strong>module </strong>full_adder  ( a, b, cin, sum , cout );

<strong> </strong>

<strong>input  </strong>a, b, cin;<strong>  output </strong>sum, cout;

<strong> </strong>

<strong>wire </strong>w0,w1,w2<strong>;</strong><strong>  </strong>

<strong> </strong>

<h1><strong>xor </strong>u0(w0,a,b); <strong> xor </strong>u1(sum,w0,cin);<strong>  </strong></h1>

<strong> </strong>

<strong>….. </strong>

<strong><sup>…..                                                                                   </sup></strong>Full_adder

<strong>….. </strong>

<strong>….. </strong>

<strong> </strong>

<strong>endmodule </strong>

<strong> </strong>

Seven-segment displays (SSD) are commonly found on computers, watches, VCRs, monitoring devices, and other electronic devices to display numbers and some characters. The seven-segment displays used in the lab consist of seven independent Light Emitting Diodes (LEDs) in the configuration of a number “8”. The different segments can be illuminated to display different numbers and letters. The segments of a seven-segment display are illustrated in the figure below. The SSDs, in general, come in packages with either a common anode or a common cathode. The SSDs on the DE10 board are common-anode. In this format the LED turns on with <strong><u>negative logic </u></strong><u>–</u> <u>i.e. low</u>.




<ol>

 <li>f) Using an <strong>always</strong> block, and <strong>if</strong>, <strong>else if</strong> and <strong>else</strong> statements place the output of your full adder on to the right-most 7-segement display in a decimal format. Remember procedural statement (like <strong>if</strong>) must be inside an <strong>always</strong> block and if there are more than one statements it must contain <strong>begin</strong> and <strong>end</strong> statements as well. The 7-segment is driven by negative logic. To turn a segment on it must be give a “0”.  Compile and download your code to the DE10 board.</li>

</ol>


