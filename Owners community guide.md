# The-Wand-Company-Pip-Boy-3000-Mk-V-Guide

## Introduction

A repository of community collaborated information, guides and tools to modify, repair and troubleshoot your Wand Company Pip boy. 

Throughout this repository will be reference to all currently known information, tools and techniques for your device. Including but not limited to repair for the internal operating system, guides to add custom files and animations and in depth references to the internal workings of the espruino board that runs the device.

All information and tools here in are open source and community created. Any work will be appropriately credited and tools created and or modified by sources outside the community, including but not limited to official tools provided by the manufacturer, shall be marked and clearly stated to be seperate while still recorded here for ease of access.

## Understanding your device

### layers of firmware and the hardware
The wand company pip-boy uses a small espruino board as the basis for its main functions, the functionality of which is broken to three levels of firmware, throughout this guide most things will only involve modifying or manipulating the first layer which is also the easiest to repair. There will however be information and guides to troubleshoot issues with the flash (second layer) or the espruinos own functions (layer 3), in most cases the fixes will only involve the first and easiest to access layer and any deviation from this will have its own section dedicated so for now lets focus on just tthe top layer. As for the rest of the hardware the pip-boy comes with a small 408x248px lcd screen, 7 buttons and dial switches to interface with the device (not including the hidden reset button), a hidden speaker and internal capacity to recieve fm transmissions. Lastly the device and its battery are charged by a usb-c connected cable that doubles as the data transfer port. This is how you will upload custom files as well as reset or updat the device using a web serial port. Its also worth noting that while plugged in once the battery is fully charged the device will bypass the battery altogether and draw power solely from the connected cable to reduce battery lifetime cycles and increase battery longevity, effectively meaning that while plugged in you could remove the battery altogether and run it solely on wall power.


### layer 1
Nestled inside your device is a small sd card that contains many of the files needed to run the device. This includes all animations, icons and sound files as well as the boot file that runs the pip-boy and flash version file. All of these together form the operating system and as such most ,odifications to the device such as custom software or settings changes will revolve around manipulating these files.

### The files
Within the sd card is a series of folders and loose files that make up the operating system or OS for short. For reference we have in this repository an archive of all past known versions. The current version is v1.29. Many who modify their pip-boy will either replace the sd card with a larger one or at the least make a copy of the sd cards stock files on their computer. In both of these instances an sd card will only work if it has the exact same files in the exact same format as the stock card, any modifications work strongly around this principle to esnure any files replaced, removed or modified are done safely without causing a corruption. Please see either the manual factory reset section or the sd card formatting section for guides to how the files should look.

## Cleaning and care
The pip-boy may need occasional dusting and this can be achieved by wiping it with a soft damp (but not wet) cloth. You can also use a microfibre cloth and a small alcohol wipe to remove finger smudges from the glass screen. Be wary of using any products especially alcohol based ones on the exterior shell as they will remove the black weathering paint and on the plastic sections potentially the silver paint as well, please see painting and weathering section for more.

## Universal Troubleshoot (try this first)

As you use your Pip-boy whether modded or stock there may be issues that arise. The following steps are designed to solve the most common issues with the device and help keep it running smoothly. If the first step fails try the second and so on.

### Troubleshooting
1. Navigate to the DATA>Maintenance tab of your device and select "reboot"
2. Hold the power button down (small button below the screen) amd keep it held until the device turns all the way off and reboots.
3. Remove the foam cuff from behind the screen side of the wrist section and look for a small hole next to the screw for the battery compartment, you may need to also remove the thin black pastic cover to see it, Both the foam cuff and black plastic piece can be returned to their place easily so dont worrry about that. Once you can see the small hole use a flattened paperclip or the blunt end of a sewing needle to instert and press the small button inside the hole, you should feel a distinct click. Once the button has been pressed the Pip-Boy should reboot and you can return the black plastic and Memory foam cuff.
4. Lastly if the above steps dont work you can try to remove and replace the battery Pin (***ONLY DO THIS IF YOU FEEL CONFIDENT, OTHERWISE SKIP TO NEXT STEP***), if you still wish to attempt this step then follow the section below on opening your device.
5. Follow the following link to erase your Pip-Boy to its factory settings. Please note this link WILL completely remove all modded, added or customised features and settings and restore your device to its manufactured state. This method MAY NOT WORK if you do not have the stock sd card installed in your device. Please skip to the section on manually resetting and restoring your device if you have already upgraded the sd card in your device. [LINK](https://thewandcompany.com/pip-boy/upgrade/2erase)

## Opening Your Pip-Boy
### Here is and in depth instructional manual onn the various steps to open your device. For ease all tasks involving these steps will be referenced here including but not limited to removing the battery for troubleshooting or upgrading your sd card
 [Deconstruction and Sd card Replacement](https://github.com/beaverboy-12/The-Wand-Company-Pip-Boy-3000-Mk-V-Guide/blob/main/Deconstruction%20and%20Sd%20card%20Replacement.md)
