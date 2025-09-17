# Basic Device Info and Troubleshooting

## Universal Troubleshoot (try this first)
As you use your Pip-boy whether modded or stock there may be issues that arise. The following steps are designed to solve the most common issues with the device and help keep it running smoothly. If the first step fails try the second and so on.

### Troubleshooting
1. Navigate to the DATA>Maintenance tab of your device and select "reboot"
2. Hold the power button down (small button below the screen) amd keep it held until the device turns all the way off and reboots.
3. Remove the foam cuff from behind the screen side of the wrist section and look for a small hole next to the screw for the battery compartment, you may need to also remove the thin black pastic cover to see it, Both the foam cuff and black plastic piece can be returned to their place easily so dont worrry about that. Once you can see the small hole use a flattened paperclip or the blunt end of a sewing needle to instert and press the small button inside the hole, you should feel a distinct click. Once the button has been pressed the Pip-Boy should reboot and you can return the black plastic and Memory foam cuff.
4. Lastly if the above steps dont work you can try to remove and replace the battery Pin (***ONLY DO THIS IF YOU FEEL CONFIDENT, OTHERWISE SKIP TO NEXT STEP***), if you still wish to attempt this step then follow the section [here](https://github.com/beaverboy-12/The-Wand-Company-Pip-Boy-3000-Mk-V-Community-Guide/blob/main/Individual%20Guides/Deconstruction%20and%20Sd%20card%20Replacement.md) on opening your device.
5. Follow the following link to erase your Pip-Boy to its factory settings. Please note this link WILL completely remove all modded, added or customised features and settings and restore your device to its manufactured state, using this link too frequently can also cause slight problems with your sd card down the line so be sure it needs it before committing. This method MAY NOT WORK if you do not have the stock sd card installed in your device. Please skip to the section on manually resetting and restoring your device if you have already upgraded the sd card in your device. [LINK](https://thewandcompany.com/pip-boy/upgrade/2erase)


## Understanding your device
Your wand company pip-boy has two layers of firmware for function. In this guide ill break down both and the hardware to a limited degree but for more complex breakdowns you can look to other sources such as the community discord or the robco website linked in the read me.

### Hardware
The wand company Pip-boy features a 320x480px lcd screen, rechargeable lipo battery, 7 buttons and knobs (excluding the reset button), an espruino microcontroller board, an fm receiver and a power cable with a female usb-c port for charging and interfacing with a computer. The screen is protected by a tritan glaze and the internals are all stored inside a body made of injection molded abs and die cast metal. The cuff is memory foam and can be adjuted slightly by adding some eva foam or a cut up sweatband behind it. 

### Pip OS
The top layer of is also known as the OS and this is the part you will interact with the most. Hosted on the sd card within the device the folders and files make up the main running of the device, Every icon and sound effect is stored here as well as files like the version that allow the next layer to function. For most people this is where any modification will happen as all apps are installed within folders at this level. Most issues also occur at this level and can be resolved with the tips in the troubleshooting section.

### Espruino firmware
The espruino firmware (and its board) are the behind the scenes part of your device, the functions here is to build the architecture that the Pip OS runs on top of. Think of it as the foundations and studs of your house with the Pip OS being everything on top. The board contains a the main firmware and then flash contains a file called .bootcde, this runs when the version in flash matches the version on the sd card and allows the device to boot. Its very rare you will come across issues with this bit but if you do there are two possible fixes if nothing else helped. 

#### Reflashing the board
Flashing is the process where you install or update the firmware installed on the board, If you encounter issues with updating your device or are forced to install a different version of the OS manually then the version stored in flash might not match the version stored on the sd card. This then causes issues with the devices ability to boot. There are a couple of options to fix this, the first is the least invasive but may not solve the issue, the second will completely reinstall the spruino firmware on the board. they are as follows:

#### Erase flash version
Power off your device altogether and then look at the front, the radio tuner knob has a button at the right most and left most position as you turn it. Turn the radio knob to the right until you feel a distinct click and hold it there, then press and hold the power button and keep both held until the device boots. This will erase the flash and copies the FW.js file from the sd card to take its place. If that doesnt work you can follow the next step to reinstall the whole espruino firmware.

#### recover corrupted espruino using dfu
To reinstall the firmware you first need to download a copy of the current OS zip or open your own backup and grab the "pipboy.bin" file. Once you have that you can either download the firmware upgrade utility [here](https://dfu-util.sourceforge.net/) or use the wand companies own web based tool [here](https://www.thewandcompany.com/pip-boy/dfu/). Once you have decided which to use you need to put your device in dfu mode, to do this you need to hold the power and torch buttons and then use a rolled out paperclip to press the hidden reset button underneath the foam cushioning next to the battery door. Once in dfu mode if you opted to install the upgrade utlity you can open a terminal at the folder where your pipboy.bin file is and run this command: "dfu-util -a 0 -s 0x08000000:leave -D pipboy.bin". If you opted to use the web version you need to follow the instructions shown on screen and that should be it, remember you need to be using a browser like chrome that supports web serial.

#### Web serial
You may see this mentioned in several places related to the device especially around updating and fixing firmware. Simply put web serial is a function in browsers like chrome that allows certain devices to have files uploaded over usb directly from your browser.

## Cleaning and care
The pip-boy may need occasional dusting and this can be achieved by wiping it with a soft damp (but not wet) cloth. You can also use a microfibre cloth and a small alcohol wipe to remove finger smudges from the glass screen. Be wary of using any products especially alcohol based ones on the exterior shell as they will remove the black weathering paint and on the plastic sections potentially the silver paint as well, please see painting and weathering Guide for more.

## Connecting to the Computer to Update and Load Apps
Your device has a usb-c female port at the end of its interface cable, this is the same port you use to charge your device. By connecting the usb to the computer instead of a wall outlet you can make changes to the device while simultaneously charging. In order to load files you will need a browser that is compatible with web serial, i use chrome but others can work too. All sites that allow you to connect the pip-boy will have a connect button that asks you to select a device (should be obvious which to select). In order to update to the latest firmware you can use the official wand company update link [Here](https://www.thewandcompany.com/pip-boy/upgrade/). Theres also an official erase tool listen in the troubleshooting section. To add, delete or replace files within your device or to download and install apps you can use the Community Pip-boy website created by Cody Tolene [here](https://pip-boy.com/)

