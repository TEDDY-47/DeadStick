#Deadzone Tool

A linear webpage which analyses a controllers stick and recommends a deadzone to mask its drift.

No installation is required. Requires the Gamepad API (Chrome, Edge and Firefox) on PC and Android.

#Instructions

1. Navigate to the webpage and attach your controller (either via USB or Bluetooth).

2. Press a button to allow the browser to recognise the controller.

3. With no movement of the sticks, click Calibrate. Data is collected for 3 seconds.

4. Review and adjust the recommended deadzone using the slider.

5. Click Copy and then paste the numbers into your games, Steam Input and/or emulator.

#Information displayed

Gray circle – unprocessed stick data

Blue circle – processed data (deadzone has been implemented)

Colourful circle – deadzone

% Drift – real time deviation of each stick

#Mechanics

Whilst calibrating, the furthest distance that each stick deviates from centre when idle is analysed. The recommended deadzone is equal to this measurement, extended by a further 15%. However, it will not exceed 50%. Once this deadzone has been radially defined, the remaining data is re-scaled to ensure that the full extent of stick motion can still be used (100%).


#Output format

Left deadzone: 7.0%
Right deadzone: 5.0%
{"left":0.070,"right":0.050}

#Run locally

Open index.html in a browser. To host it, enable GitHub Pages on the repo (Settings, Pages, deploy from the main branch).

#Notes

• Some browsers only detect a controller after a button press.
• Mapping assumes standard layout: axes 0/1 left stick, 2/3 right stick.
• It reads and suggests values only. It doesn't write to your system or game configs.

#Related

Part of the Ghostick tools: Ghostick, the controller tester.