# VDSCalculator
Performs calculations for key experiments related to drug screening and DNA/protein purification

## DSF
Differential Scanning Fluorimetry, or DSF, is an experiment that is used for initial high throughput screening to find a potential drug that binds to a target protein by determining the melting points of the protein with and without the possible drug binded. Samples are created with a mixture of chemicals and proteins to determine these melting points at different protein concentrations. There are 3 main "ingredients" in DSF:

### Elutions
The target protein is purified after being grown as cell culture, and its protein concentration is documented in Elution 1 and Elution 2. Elution 1 mostly has the purified protein with some extra cell debris, and Elution 2 should only have the purified protein. It is common to use Elution 1 since more target protein is usually there, but Elution 2 can work better at times.

This first section covers the calculations for determining the amount of purified target protein to be used in each sample based on the concentration.
* `intro_questions` function to determine the total number of unique elutions (as previous purification elutions can be used)
* `elution_questions` function to determine which elution is being used
* `loop_concentrations` function to perform calculations for each desired final protein concentration
* `print_table` function to print the table of measurements
* `run_dsf_calcs` function to perform all calculations for every elution

### Controls
There are positive and negative controls to ensure that the experiment was performed correctly. The positive is lysozyme, which breaks down enzymes, and the negative is water.

This next section covers the calculations for determining the amount of each chemical needed to make a big batch of controls for a desired number of samples
* `intro2_questions` function to determine the total number of controls
* `do_calcs` function to perform the calculations
* `print_ctrl_table` function to print the table of measurements
* `ctrl_calcs` function to perform all functions in one

### Sypro
Sypro is a light-sensitive dye that is crucial in performing this experiment and is in every sample.

This last section covers the calculations for creating a 200x concentration from a 5000x stock concentration.
* `sypro_intro` function to determine the total number of samples
* `sypro_math` function to perform the calculations
* `sypro_print_table` function to print the table of measurements
* `sypro_calc` function to perform all functions in one

### Print All Tables
This pulls all the tables for one round of the experiment for easy accessibility.

* `print_df_tables` function to print every table saved
