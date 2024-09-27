java c
EE 210
Laboratory 03
Fall semesterThis laboratory activity is a tutorial for Multisim (Version 14.2), a circuit simulation software package by National Instruments that allows you to graphically build circuit schematics, to simulate the network, and to analyze the network response. Multisim also has a number of virtual lab instruments that you can use to test your circuits just as you would on the bench with real instruments.  It is important to become familiar with this software because it will be used in several of the subsequent labs to verify manual network analyses.  Due to the tutorial nature of this lab, your submissions are different than for other labs. Follow the directions below:· Lab Submission: You will not have a prelab or lab worksheet to complete.  Instead, you will submit the following items at the beginning of your next lab meeting:· Screen shots of simulation measurements, as requested· Screen shots of virtual oscilloscope displays, as requested· Excel plots, as requestedThis lab activity is not a group submission. Each student is expected to do and submit their own work.

In-Lab Activities:Activity 1:  DC analysis of a passive DC network
In this experiment you will be introduced to the DC analysis capabilities of Multisim.  You will use virtual multimeters and wattmeters to test your circuit.  You will learn how to run an interactive simulation as well as a DC Operating Point Analysis.

Figure 1: Passive DC Network
1.  Launch Multisim and model the schematic in Figure 1 above.
a. Place the resistors:         
i. Select the “Place Basic” button.  The “Select a Component” window will open.  For the remainder of this lab, if you have any doubt about what a button is, mouse over it and a tooltip with its name will appear.
ii. In the “Family” column, highlight “Resistor”.
iii. In the “Component column, highlight or type “5k” and press OK.
iv. Position the ghost resistor and click to place a resistor on the schematic.
v. The “Select a Component” window will reopen.  Select a 10k resistor.  Click OK to place the second resistor.
b. Place the voltage source:                  
i. From the “Select a Component” window, set “Group” to “Sources”.
ii. In the “Family” column, highlight “Select all families”.
iii. In the “Component column, highlight “DC_POWER” and press OK.
iv. Position the ghost DC power supply and click to place it on the schematic.
c. Place the current source in the same manner as the voltage source, but select “DC_CURRENT” from the “Component” column.
d. Place the ground in the same manner as the voltage source, but select “GROUND” from the “Component” column.
e. Select Close or hit ESC when the “Select a Component” window reopens to end the part placement mode.
f. Arrange the parts to roughly match Figure 1.
i. To move a part, click and drag it.
ii. To rotate a part 90 degrees hit CTRL+R while it is selected.
g. Connect the parts:
i. Click on the terminals of each part to place a wire.
ii. (To place a wire manually key CTRL+Q).
h. Change the voltage value for the voltage source.
i. Double-click on the voltage source and a properties panel will open.
ii. Select the “Value” tab, if it is not already selected.
iii. Change the voltage to 6V.
i. Specify the current value for the current source using the same procedure as for the voltage source.  Set the current source to 3mA by entering either ‘0.003’ or ‘3m’ in the current box.  You can specify any multiplier units manually using k(kilo), m(milli), u(micro), etc. 
2.  Set up virtual DMMs to monitor the network voltages and currents:                
a. Place a DMM to measure the voltage Va.
i. Select the Multimeter icon from the “Instruments” toolbar on the far right.
ii. Click to place it on your schematic.
iii. Connect it as you would a real DMM for the voltage measurement.
iv. Double-click on the DMM and set it to measure DC voltage.  Leave the measurement window open.
b. Place another DMM to monitor the voltage Vb across the 10k resistor.
c. Place a third DMM to monitor the current Ia.
i. Select the Multimeter button from the “Instruments” toolbar.
ii. Click to place it on your schematic.
iii. Double-click on the DMM and set it to measure DC current.  You will always want to perform. this step prior to connecting a DMM for current measurements to your circuit to minimize simulation errors.
iv. Connect it as you would a real DMM for the current measurement.
3. Run the simulation by selecting the green “Play” button. Save a screen capture image showing the schematic with these measurements. You will submit this as part of your lab submission. Stop the simulation by selecting the red “Stop” button.                  
4. Set up a virtual wattmeter to measure the power dissipated by R1 and R2.           
a. Remove the virtual DMMs.
b. Place a wattmeter to measure the power dissipated by R1.
i. Select the wattmeter icon from the “Instruments” toolbar.
ii. Connect the voltage portion in parallel with R1.
iii. Connect the current portion in series with R1.
iv. Double click on the wattmeter to display the screen.
c. Place another wattmeter to measure the power dissipated by R2.
d. Re-run the simulation by selecting the green “Play” button. Save a screen capture image showing the schematic with these measurements. You will submit this as part of your lab submission. Stop the simulation by selecting the red “Stop” button.
5. You can also run a DC analysis which will automatically measure all desired parameters for you.  The steps for doing this are as follows.
a. Remove all of the measurement devices from your circuit model and repair any broken network connections.
b. Rename the network branch between R1, R2, and I1.
i. Select the “Nets” tab in the Spreadsheet View window.
ii. Select the Net that highlights the network branch between R1, R2, and I1.
iii. Click the box located in the “Net name” column () to open the Net Properties window.
iv. Specify the network name in the “Preferred net name” text box, located in the “Net name” tab (e.g. Va). 
v. Ensure the ‘Show net name’ check box is checked.
vi. Click Apply, then OK to close the properties window.
c. Repeat step b, and rename the network branch between V1 and R1 (e.g. Vin).
d. Select “Simulate” from the main menu bar.
e. Select Analysis and simulation.  Highlight ‘DC Operating Point’ in the Active Analysis table on the left.  The DC Operating Point Analysis menu will open on the right-hand side.  This menu will contain a list of voltage, current and power variables for each node/component.  Multisim assigns a number to each node; if you did not assign your own name in the previous steps, you will need to determine Multisim’s nodal numbering system to measure the correct values in the following steps.
f. To measure Va, select and add this node’s associated voltage variable to the list of output variables (e.g. V(Va)).
g. To measure Vb (or any voltage that is not a node voltage) you will need to select “Add Expression” and then enter a mathematical expression to calculate the desired voltage (e.g. “V(Vin)-V(Va)”).
h. To measure the current Ia, add the variable I(V1) to the list of output variables.  This calculates the current through the voltage source labeled V1.   NOTE:  Passive sign convention is used, so I(V1) is actually –Ia.  
i. To measure the power dissipated by each resistor, add the variables P(R1) and P(R2) to the list of output variables. 
j. When your “Selected Variables for Analysis” list contains variables associated with Va, Vb, I(V1)), P(R1), and P(R2), click the simulate button. Verify the results which are displayed agree with those you measured earlier. Save a screen capture image showing the table with these measurements. You will submit this as part of your lab submission. Stop the simulation by selecting the red “Stop” button. 
6. Save your schematic to a convenient location by selecting File>Save As> . Type the desired file name “Lab03_DC” 
Activity 2:  Transient analysis of a passive AC network
In this experiment you will be introduced to the transient analysis capabilities of Multisim.  You will use a virtual function generator to provide an input to your circuit and a virtual oscilloscope to view voltages in your circuit.  You will also learn how to export transient waveform. measurement data to a spreadsheet.
1. Open a 2nd instance of your existing schematic and give it new name.
a. On the main toolbar select File>Open and then navigate to your Lab03_DC file.
b. Save this 2nd schematic (which you will be changing) as “Lab03_AC”. 
2. Replace the DC voltage source with a virtual function generator.                
a. Remove the DC voltage source from your schematic.
b. Select the Function Generator icon from the “Instruments” toolbar and place it代 写EE 210 Laboratory 03 Fall semester
代做程序编程语言 on your schematic.
i. Double-click on the function generator.  Set it to 1kHz sine wave with an amplitude of 5V (this means the sine wave will be 10 V peak-to-peak).
ii. Connect it to your circuit using the “+” terminal on the left for the positive lead and the center “com” terminal for ground.  (Leave the “-” terminal on the right unconnected.) 
(FYI:  If you want a more realistic function generator interface, there exists a model for an Agilent function generator on the “Instruments” toolbar.  This function generator’s knobs/buttons/controls are like those on an actual Agilent 33120A.  If you are more comfortable with this more realistic function generator, you may use it instead.  Make sure to note that when using THIS function generator model instead of the generic one, the signal voltage you define is Vpp, not V amplitude, so if you want a 5 V amplitude sine wave you would enter 10 Vpp as your “amplitude.”)
3.  Set up a virtual oscilloscope to measure the output of the function generator on channel A and Va on channel B:                   
a. Place a virtual oscilloscope on your schematic.
i. Select the general Multisim oscilloscope icon from the “Instruments” toolbar.  The icon is labeled “Oscilloscope.”
ii. Click to place it on your schematic.
iii. Connect the + terminal on Channel A to the output of your function generator. Connect the – terminal on Channel A to ground.
iv. Connect Channel B to measure Va. Make sure to connect both the + and – terminals, as you did with Channel A.
v. Change the color of the Va network branch.
a. Under the Nets tab of the Spreadsheet view, select the Va net from the list and click the color column to enable the color selection for the Va net.
b. Click the drop-down arrow and select a color (other than the default red).  You may choose ‘other’ if you wish to choose from a wider array of colors than shown.
vi. Double click on the oscilloscope to display its screen and controls.
(FYI: If you want a more realistic oscilloscope interface, there exists models for both Agilent and Tektronix oscilloscopes on the “Instruments” toolbar. The knobs/buttons/controls match those of their physical oscilloscope counterparts. Note that these models don’t have a negative (--) terminal for the scope input. They only have a + connection and the voltage is always displayed with respect to ground. The Tektronix model has a separate G terminal that needs to be connected to circuit ground.)
4. Run the simulation by selecting the green “Play” button.
a. The colors for Channel A and Channel B on the oscilloscope display will match the associated net colors you selected earlier.
b. While the simulation is running, you can adjust the display:
i. Set the vertical scales for both Channel A and Channel B to 10 V/div
ii. Adjust the Timebase scale to display a few complete cycles of the input and output signals.
iii. Make sure that the trigger is set to rising edge trigger on Channel A with a trigger level of 0 V. Setting the trigger type to “Normal” will result in a constantly-refreshing display. Setting the trigger type to “Single” will result in the display of a single sweep.
iv. You can pause the simulation at any time to freeze the display.
v. Two vertical measurement bars on the left edge of oscilloscope screen can be moved anywhere on the screen to get an accurate readout of any points on the displayed signals. The window below the oscilloscope screen displays the measurement bar values. Place one bar at a point where Channel B is maximum and place the other bar at a point where Channel B is minimum. This allows you to determine the peak-to-peak amplitude of the signal.
vi. With the peak-to-peak measurement displayed, save a screen capture of the oscilloscope display showing this measurement. You will submit this as part of your lab submission. Stop the simulation by selecting the red “Stop” button.
Activity 3:  DC analysis of an active DC network
In this exercise you will learn how to use a dependent source in simulation.Figure 2: Active DC Network
1. Open a new project.
a. On the main toolbar select File>New
b. Create a Blank workspace
c. Save it as “Lab03_ACTIVE” 
2. Model the schematic in Figure 2.
a. To place a voltage controlled current source:
i. Set “Group” to “Sources” button in the “Select a Component” window.
ii. In the “Family” column, highlight “CONTROLLED_CURRENT”
iii. Select the VOLTAGE_CONTROLLED_CURRENT_SOURCE and place it on your schematic.
iv. Connect it as in Figure 3.  You will be measuring the voltage across R1 as a reference for your voltage dependent source.
a. To flip a part vertically hit ALT+Y while it is selected.

Figure 3: Active DC Network (Multisim View)
3. Set the transconductance of your dependent source to 0.002 Mho.  Transconductance (G) = 1/(Resistance).  The unit of transconductance is Mho = 1/Ohm so that:Volts*Mho = Volts/Ohm = Amps 
4. Set up DMMs to measure the voltages Va and Vb.
5. Set up another DMM to measure the current Ia exiting the voltage source.  Pay particular attention to the orientation of your “+” and “-“ terminals so that you get the current sign right.
6. Run the simulation by pressing the green “Play” button. Save a screen capture image showing this schematic and DMM measurements. You will submit this as part of your lab submission. Stop the simulation by selecting the red “Stop” button. 
Activity 4: Dealing with Operational Amplifiers (a preview of things to come)

In this exercise, you will get a first look at operational amplifiers, a topic that we’ll be covering in class shortly. You will also learn how to export simulation data to Excel for later analysis/plotting.
1. Download “Opamp_Lab_03” from Canvas.  This file illustrates how to connect operational amplifier models in Multisim.
2. Use the virtual DMM to take the following measurements and determine the gain of the circuit (Vout/Vin).
a. I1
b. I2
c. I3
d. Vout
3. Save a screen capture image showing the schematic and DMM measurements. You will submit this as part of your lab submission. 
4. Replace the 1 Volt DC power supply with a signal generator.
o Set the signal generator to a sine wave with 1 Volt amplitude (2 V Peak-to-Peak amplitude), 5kHz, 0V DC offset.
o Use the generic Multisim oscilloscope to capture Vin on channel 1 and Vout on channel 2.
o Change the Interactive Simulation Settings to run for only 5 periods of the 5kHz input signal (1 ms). The reason that we only want to run the simulation for 5 periods is because we will be saving the data to an Excel file and don’t want to generate more data than we need.
§ On the main menu go to Simulate>Analysis and simulation.
§ Highlight ‘Interactive Simulation’ in the Active Analysis table and, under the analysis parameters tab, change End time (TSTOP) to 0.001 s.
5. You can export simulation data to Excel in table-form. for later analysis or more sophisticated plotting. The instructions for doing so are below. Note: In order to capture the data you must use the general Multisim oscilloscope, not one of the special scopes.             
a. Click the green “Play” button to run your simulation. 1 ms worth of data will be generated.
b. Click the “Grapher” button on the “Main” toolbar. Your oscilloscope display will now show up in a separate “Grapher” window.
i. Export your data to an Excel spreadsheet by going to Tools>Export to Excel on the main menu of the Grapher View window.
ii. Select both sets of data and click “OK”
iii. Your data should now be conveniently displayed in an Excel spreadsheet.
6. Using the Excel data, plot Vout vs Vin.  Make sure to include an appropriate title and axis labels.  Measure the slope of the line you have plotted. What do you think this line represents?  (It is possible that you will see two parallel lines -- this is the result of a capacitance effect causing a phase shift between input and output. It is not an issue that you need to worry about).
7. Save a screen capture image and submit a copy of your Excel graph. Include the calculation of the line slope and an explanation of what the slope of the graph seems to represent for this circuit.
8. Now replace R2 with a resistor of value 100 kΩ and repeat steps 4 - 5 (only measure the slope of the center region).  
9. Save a screen capture image and submit a copy of your Excel graph. Include the calculation of the line slope and an explanation of what the slope of the graph seems to represent for this circuit. Also include a brief discussion what additional phenomenon is being shown on the graph. 
Summary of items to be submitted- Four schematic screenshots (two from activity 1, activity 3, activity 4)- One table screenshot (activity 1)- One oscilloscope screenshot (activity 2)- Two Excel graphs with discussions (activity 4)

         
加QQ：99515681  WX：codinghelp
