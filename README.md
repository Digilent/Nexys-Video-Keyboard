Nexys Video Keyboard Demo
==============

Description
--------------
This project is a Vivado demo using the Nexys Video's USB HID Host port and USB UART bridge, written in Verilog. When programmed onto the board, whenever the user presses a key on a keyboard connected to the USB HID port (J15, labeled "USB HOST"), a scan code is sent to the Nexys Video through a PS/2 interface. This scan code is read and transmitted to the computer via the USB-UART bridge. When the key is released, a scan code of 0xF0XX is transmitted, indicating that the key with PS/2 code "XX" has been released.

To use this demo, the Nexys Video must be connected to a serial terminal on the computer it is connected to over the MicroUSB cable. For more information on how to set up and use a serial terminal, such as Tera Term or PuTTY, refer to [this tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).

For example: If the user presses the space bar on a keyboard connected to the Nexys Video, the scan code "29" will be sent to the computer.  When the space bar is released, "F0 29" will be printed.

Requirements
--------------
* **Nexys Video**: To purchase a Nexys Video, see the [Digilent Store](https://store.digilentinc.com/nexys-video-artix-7-fpga-trainer-board-for-multimedia-applications/)
* **Vivado 2018.2 Installation**: To set up Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **Serial Terminal Emulator**: For more information, see the [Installating and Using a Terminal Emulator Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).
* **MicroUSB Cable**
* **USB Keyboard**

Demo Setup
--------------
1. Download and extract the most recent release ZIP archive from this repository's [Releases Page](https://github.com/Digilent/Nexys-Video-Keyboard/releases).
2. Open the project in Vivado 2018.2 by double clicking on the included XPR file found at "\<archive extracted location\>/vivado_proj/Nexys-Video-Keyboard.xpr".
3. In the Flow Navigator panel on the left side of the Vivado window, click **Open Hardware Manager**.
4. Plug a Nexys Video into the computer running Vivado using a MicroUSB cable.
5. Open a serial terminal emulator (such as TeraTerm) and connect it to the Nexys Video's serial port, using a baud rate of 9600.
6. In the green bar at the top of the window, click **Open target**. Select **Auto connect** from the drop down menu.
7. In the green bar at the top of the window, click **Program device**.
8. In the "Program Device" Wizard, enter "\<archive extracted location\>vivado_proj/Nexys-Video-Keyboard.runs/impl_1/top.bit" into the "Bitstream file" field. Then click **Program**.
9. The demo will now be programmed onto the Nexys Video. See the Introduction section of this README for a description of how this demo works.

Next Steps
--------------
This demo can be used as a basis for other projects, either by adding sources included in the demo's release to those projects, or by modifying the sources in the release project.

Check out the Nexys Video's [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/nexys-video/start) to find more documentation, demos, and tutorials.

For technical support or questions, please post on the [Digilent Forum](https://forum.digilentinc.com).

Additional Notes
--------------
For more information on how this project is version controlled, refer to the [Digilent Vivado Scripts Repository](https://github.com/digilent/digilent-vivado-scripts)

<!--- 03/12/2019(ArtVVB): Validated in hardware with Vivado 2018.2 --->