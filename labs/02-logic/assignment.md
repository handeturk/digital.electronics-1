
# Lab 2: HANDE_TURK

### 2-bit comparator

1. Karnaugh maps for other two functions:

   Greater than:

   ![WhatsApp Image 2022-02-23 at 23 43 52](https://user-images.githubusercontent.com/99410897/155422277-66c05349-09e0-42c8-95ca-28fe3492475b.jpeg)


   Less than:

   ![K-maps](images/kmap_empty.png)

2. Equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   ![Logic functions](images/comparator_min.png)

### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **xxxx??**

```vhdl
     p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started" severity note;

        -- First test case
        s_b <= "0011"; -- ID = xxxx35
        s_a <= "0101"; -- ID = xxxx35
       wait for 100 ns;
              
        -- Expected output
          assert ((s_B_greater_A = '0') and
                (s_B_equals_A  = '0') and
                  (s_B_less_A    = '1'))
        -- If false, then report an error
        report "Input combination 00, 00 FAILED" severity error;


        -- Report a note at the end of stimulus process
        report "Stimulus process finished" severity note;
        wait;
    end process p_stimulus;
```

2. Text console screenshot during your simulation, including reports.

   ![Ek Açıklama 2022-02-24 013546](https://user-images.githubusercontent.com/99410897/155421902-adca8bd5-f55e-48f8-904b-1caf0aa93eba.png)



3. Link to your public EDA Playground example:

  https://www.edaplayground.com/x/Nbvg
