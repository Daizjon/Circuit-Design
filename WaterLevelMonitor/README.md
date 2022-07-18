Designed an indicator for a water level monitor in a nuclear power plant spent fuel pool. The water level is indicated by a value 0-4, where 0 is no water, and 4 is 40 feet of water. There are four water level sensors, each providing an input pin to the circuit. The first one is at 10'. The next at 20', and so forth up to 40'. The pins detect water, so if the water is at 40', all of the pins will signal detection (water = logical 1, no water = logical 0). If you detect an inversion (40' is triggered, but 20' is not, or so) then display an 'E' on the 8-segment display.

Also designed an indicator for the control panel using an 8-segment display.

Designed the logic that displays a 1 if and only if the water level is at 10'. If no water is detected, signal 0. Otherwise, signal where the water level is the highest, up to 40'.

The 7-segment display in Logisim connects using the following pins. So, for example, to display a 4 (for 40' of water), I illuminated segments 0, 1, 3, and 6, and an error would illuminate segments 0, 1, 2, 4, and 5.
