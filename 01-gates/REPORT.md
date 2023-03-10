# Lab 1: Tomáš Calábek

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

   ![Logic function](/01-gates/rovnice.png)

2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of gates is
begin
    f_orig_o  <= (not(b_i) and a_i) or (not(c_i) and not(b_i));
    f_nand_o <= ((a_i nand not(b_i)) nand (not(b_i) nand not(c_i)));
    f_nor_o  <= (b_i nor (a_i nor not(c_i)));
end architecture dataflow;
```

3. Complete table with logic functions' values:

   | **c** | **b** |**a** | **f_ORIG** | **f_(N)AND** | **f_(N)OR** |
   | :-: | :-: | :-: | :-: | :-: | :-: |
   | 0 | 0 | 0 | 1 | 1 | 1 |
   | 0 | 0 | 1 | 1 | 1 | 1 |
   | 0 | 1 | 0 | 0 | 0 | 0 |
   | 0 | 1 | 1 | 0 | 0 | 0 |
   | 1 | 0 | 0 | 0 | 0 | 0 |
   | 1 | 0 | 1 | 1 | 1 | 1 |
   | 1 | 1 | 0 | 0 | 0 | 0 |
   | 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![your figure](/01-gates/Screenshot_1.jpg)

2. Link to your public EDA Playground example:

   [https://www.edaplayground.com/x/6vNE]
