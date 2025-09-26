# Basic Device Info and Troubleshooting

## Universal Troubleshoot (try this first)

As you use your Pip-Boy, whether modded or stock, there may be issues that
arise. The following steps are designed to solve the most common issues with the
device and help keep it running smoothly. If the first step fails, try the
second and so on.

### Troubleshooting

**Navigate to the DATA > Maintenance tab of your device and select "reboot".**

**Step 1: Hold the power button down (small button below the screen) and keep it
held until the device turns all the way off and reboots.**

**Step 2: Remove the foam cuff from behind the screen side of the wrist section
and look for a small hole next to the screw for the battery compartment. You may
need to also remove the thin black plastic cover to see it. Both the foam cuff
and black plastic piece can be returned to their place easily, so don't worry
about that. Once you can see the small hole, use a flattened paperclip or the
blunt end of a sewing needle to insert and press the small button inside the
hole—you should feel a distinct click. Once the button has been pressed, the
Pip-Boy should reboot and you can return the black plastic and memory foam
cuff.**

**Step 3: Lastly, if the above steps don't work, you can try to remove and
replace the battery pin (\***ONLY DO THIS IF YOU FEEL CONFIDENT, OTHERWISE SKIP
TO NEXT STEP**\*). If you still wish to attempt this step, then follow the
section [here][teardown-and-sd] on opening your device.**

**Step 4: Follow the link to erase your Pip-Boy to its factory settings. Please
note this link WILL completely remove all modded, added, or customized features
and settings and restore your device to its manufactured state. Using this link
too frequently can also cause slight problems with your SD card down the line,
so be sure it needs it before committing. This method MAY NOT WORK if you do not
have the stock SD card installed in your device. Please skip to the section on
manually resetting and restoring your device if you have already upgraded the SD
card in your device. [LINK][twc-reset]**

## Understanding your device

Your Wand Company Pip-Boy 3000 Mk V has two layers of firmware for function. In
this guide I'll break down both and the hardware to a limited degree, but for
more complex breakdowns you can look to other sources such as the community
Discord or the RobCo Industries website linked in the readme.

### Connecting to the Computer to Update and Load Apps

Your device has a USB-C female port at the end of its interface cable; this is
the same port you use to charge your device. By connecting the USB to the
computer instead of a wall outlet, you can make changes to the device while
simultaneously charging. In order to load files, you will need a browser that is
compatible with Web Serial. I use Google Chrome, but others can work too. All
sites that allow you to connect the Pip-Boy will have a Connect button that asks
you to select a device (should be obvious which to select). In order to update
to the latest firmware you can use the official Wand Company upgrade page
[here][twc-upgrade]. There's also an official erase tool listed in the
troubleshooting section. To add, delete, or replace files within your device—or
to download and install apps—you can use the Community Pip-Boy website created
by Cody Tolene [here][pip-boy-website].

### Hardware

The Wand Company Pip-Boy features a 320×480 px LCD screen, rechargeable LiPo
battery, 7 buttons and knobs (excluding the reset button), an Espruino
microcontroller board, an FM receiver, and a power cable with a female USB-C
port for charging and interfacing with a computer. The screen is protected by a
Tritan glaze, and the internals are all stored inside a body made of injection-
molded ABS and die-cast metal. The cuff is memory foam and can be adjusted
slightly by adding some EVA foam or a cut-up sweatband behind it.

### Pip OS

The top layer is also known as the OS, and this is the part you will interact
with the most. Hosted on the SD card within the device, the folders and files
make up the main running of the device. Every icon and sound effect is stored
here, as well as files like the version that allow the next layer to function.
For most people this is where any modification will happen, as all apps are
installed within folders at this level. Most issues also occur at this level and
can be resolved with the tips in the troubleshooting section.

### Espruino firmware

The Espruino firmware (and its board) is the behind-the-scenes part of your
device. The function here is to build the architecture that the Pip OS runs on
top of. Think of it as the foundations and studs of your house, with the Pip OS
being everything on top. The board contains the main firmware and then flash
contains a file called `.bootcde`. This runs when the version in flash matches
the version on the SD card and allows the device to boot. It's very rare you
will come across issues with this part, but if you do there are two possible
fixes if nothing else helped.

#### Reflashing the board

Flashing is the process where you install or update the firmware installed on
the board. If you encounter issues with updating your device or are forced to
install a different version of the OS manually, then the version stored in flash
might not match the version stored on the SD card. This then causes issues with
the device’s ability to boot. There are a couple of options to fix this: the
first is the least invasive but may not solve the issue; the second will
completely reinstall the Espruino firmware on the board. They are as follows:

#### Erase flash version

Power off your device altogether and then look at the front. The radio tuner
knob has a button at the rightmost and leftmost positions as you turn it. Turn
the radio knob to the right until you feel a distinct click and hold it there,
then press and hold the power button and keep both held until the device boots.
This will erase the flash and copy the `FW.js` file from the SD card to take its
place. If that doesn’t work, you can follow the next step to reinstall the whole
Espruino firmware.

#### Recover corrupted Espruino using DFU

To reinstall the firmware, you first need to download a copy of the current OS
ZIP or open your own backup and grab the `pipboy.bin` file. Once you have that,
you can either download the firmware upgrade utility [here][dfu-util] or use The
Wand Company’s own web-based tool [here][twc-dfu]. Once you have decided which
to use, you need to put your device in DFU mode. To do this, hold the power and
torch buttons and then use a rolled-out paperclip to press the hidden reset
button underneath the foam cushioning next to the battery door. Once in DFU
mode, if you opted to install the upgrade utility, open a terminal at the folder
where your `pipboy.bin` file is and run this command:
`dfu-util -a 0 -s 0x08000000:leave -D pipboy.bin`. If you opted to use the web
version, follow the instructions shown on screen and that should be it. Remember
you need to be using a browser like Google Chrome that supports Web Serial.

#### Web Serial

You may see this mentioned in several places related to the device—especially
around updating and fixing firmware. Simply put, Web Serial is a feature in
browsers like Google Chrome that allows certain devices to have files uploaded
over USB directly from your browser.

## Cleaning and care

The Pip-Boy may need occasional dusting, and this can be achieved by wiping it
with a soft damp (but not wet) cloth. You can also use a microfiber cloth and a
small alcohol wipe to remove finger smudges from the glass screen. Be wary of
using any products, especially alcohol-based ones, on the exterior shell as they
will remove the black weathering paint and, on the plastic sections, potentially
the silver paint as well. Please see the [Painting and
Weathering][painting-and-weathering] guide for more.

<!-- INTERNAL LINKS -->

[painting-and-weathering]:
  https://github.com/beaverboy-12/The-Wand-Company-Pip-Boy-3000-Mk-V-Community-Guide/blob/main/Individual%20Guides/Painting%20and%20Weathering.md
[teardown-and-sd]:
  https://github.com/beaverboy-12/The-Wand-Company-Pip-Boy-3000-Mk-V-Community-Guide/blob/main/Individual%20Guides/Deconstruction%20and%20Sd%20card%20Replacement.md

<!-- EXTERNAL LINKS -->

[dfu-util]: https://dfu-util.sourceforge.net/
[pip-boy-website]: https://www.pip-boy.com/
[twc-dfu]: https://www.thewandcompany.com/pip-boy/dfu/
[twc-reset]: https://thewandcompany.com/pip-boy/upgrade/?erase
[twc-upgrade]: https://www.thewandcompany.com/pip-boy/upgrade/
