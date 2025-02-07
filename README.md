# HP_Probook_440_G5_Prot
12V switch to protect the LCD backlight for HP Probook 440 G5 Notebook

-----

The HP Probook 440 G5 notebook has a very simple LCD backlight power supply scheme.
The motherboard sends 12 V directly to the screen, even when the notebook is turned off.

Due to a "leakage" of electrical current in the backlight LEDs, the backlight may occasionally turn on when the notebook is turned off.

The LCD has a control board, which receives the 12V and raises it to 24V in a DC-DC circuit.

When the BLON_CON signal is 0V, the DC-DC stops raising the voltage (24V), but the LEDs still continue to receive 12V.

![img](https://raw.githubusercontent.com/rtek1000/HP_Probook_440_G5_Prot/refs/heads/main/Img/Display_adapter.png)

If the display works well when the notebook is on, but when the notebook is off, the battery charge lasts a short time and the backlight turns on, it may be possible to apply this adaptation.

It is necessary to remove the 0R resistor number R7725 in the schematic. This resistor is very easy to locate and there should be electrical continuity (using a multimeter) with pin 1 of the LCD ribbon cable connector.

![img](https://raw.githubusercontent.com/rtek1000/HP_Probook_440_G5_Prot/refs/heads/main/Img/Schematic1.png)
