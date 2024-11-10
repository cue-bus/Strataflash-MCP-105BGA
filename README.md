# Strataflash-MCP-105BGA
Breakout adapters for Intel/Numonyx Strataflash MCP chips in 105BGA package

These adapters can be used to interface with these BGA chips using standard chip programmers such as the XGecu T56. The breakouts feature a NOR section and NAND section if the chip has it. The chips' NOR sections have been successfully read using a T56 programmer using the Micron MT28GUxxxAAA2EGC algorithm, where xxx is the size of the die to be read. Note that the T56 will complain both about unconnected pins as well as the incorrect chip ID. To get the T56 to read them, you can uncheck the "Pin Check" and "Check ID" options and the read will still be successful. 
For the NOR section, make sure to use the 8 pin cable that connects the ISP header to the 8 extra pins in the NOR section. Make sure to respect pin 1 orientation on both ends.

Since these chips have up to 4 different dies, you can cycle through each CE line one by one. Select the CE jumper for the die you want to read (CE1 and 2 for NOR, CE3 and 4 for NAND) by soldering the center pad to the left pad. Solder the other CE center pads to the right, which connects them to VCC and holds them unasserted. Make sure you do not have more than 1 CE center pad jumpered to the left.
