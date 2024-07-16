<div align="left">
  <img src="https://github.com/user-attachments/assets/0d62ee59-bee5-4ca9-823c-5f045ca780e5" alt="Bechoff TwinCat" width="700"/>
</div>

<div align="left">
  <a href="https://www.beckhoff.com/en-en/products/automation/twincat/" target="_blank">
    <img src="https://img.shields.io/badge/TwinCAT-3.1.4024.55-blue" alt="TwinCAT 3.1.4024.55"></a>
  <a href="https://github.com/Dalageo/TwinCat-VirtualWasher/blob/main/LICENSE" target="_blank">
    <img src="https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey" alt="License: CC BY-NC-SA 4.0"></a>
  <img src="https://img.shields.io/github/stars/Dalageo/TwinCat-VirtualWasher?style=social" alt="GitHub stars">
</div>

# Simulating a Washing Machine System with TwinCAT PLC Programming

This repository contains a simulation project for a Washing Machine System, developed within the <a href="https://www.beckhoff.com/en-en/products/automation/twincat/"> TwinCAT </a> environment as part of a master's course assignment at <a href="https://www.hv.se/en/">University West</a>. The assignment involves developing the control logic for specific functions of a washing machine, with the `PLCSim` program, including the `Visualization.TcVIS`, provided by the university. The designed washing machine system includes the following functionalities:</p>

- **System Activation and Deactivation**: The washing machine is turned on by rotating the switch to the *START* position. The process can be stopped at any time by rotating the switch to the *STOP* position.
- **Water Filling**: The user can select the desired water filling level, either *LEVEL2* (NORM) or *LEVEL3* (HIGH), by turning the *LEVEL* rotary switch.
- **Temperature Control**: Once the water reaches the selected level, the *HEATER* operates until the *CURRENT TEMP* matches the *SET TEMP* on the `Visualization.TcVIS`. The heater dynamically adjusts to keep the *CURRENT TEMP* within the *TEMP OK* range.
- **Washing Cycle**: When the desired temperature is reached, the washing machine begins the washing cycle by spinning the washer cylinder forward for 5 seconds and then backward for another 5 seconds.
- **Heater Failure**: If the heater fails, the washing machine stops and will not resume until the temperature is back within the appropriate range.
- **Water Draining**: When the washing cycle ends, the machine drains all the water until the drum is empty.
- **Cycle Completion and Restart**: Upon completing a cycle, the program waits for user input. If the *PULS* button is pressed, the cycle repeats continuously until the button is released.

| Washer | 
|-----|
| ![Washer](https://github.com/user-attachments/assets/8ca00285-1202-4bf2-b5be-3040479dc957) | 

## Setup Instructions

1. **Download and Install:**
   [TwinCAT 3 download | eXtended Automation Engineering (XAE)](https://www.beckhoff.com/en-en/support/download-finder/search-result/?download_group=97028248&download_item=650023470)
   
2. **Clone the repository:**
   ```sh
   git clone https://github.com/Dalageo/TwinCAT-VirtualWasher.git
   
3. **Navigate to the cloned directory and execute the 'TwinCAT Virtual Washer.sln' solution file.**

4. **Navigate to TwinCAT directory and execute Start.bat**:
   ```sh
   C:/TwinCAT/3.1/Runtimes/UmRT_Default/Start.bat

5. **Change the Target System in TwinCAT to UmRT_Default.**
   
6. **Activate Configuration.**
   
7. **Login and Start both 'PLCSim' and 'PLCStudent'.**
  
## Contributions

This project was part of a master course assignment at [University West](https://www.hv.se/en/), which provided the initial codebase for <code>PLCSim</code>. Special thanks to the professors at University West who contributed to its development.

## License

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). It was chosen to prevent commercial use and to promote free access and open collaboration, ensuring any adaptations remain freely available to everyone.

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

## Citation

```bibtex
@software{Dalageorgos_TwinCAT-VirtualWasher_2024,
author = {Dalageorgos, Konstantinos},
license = {CC-BY-NC-SA-4.0},
month = jul,
title = {{TwinCAT-VirtualWasher}},
url = {https://github.com/Dalageo/TwinCAT-VirtualWasher},
version = {1.0.0},
year = {2024}
}
