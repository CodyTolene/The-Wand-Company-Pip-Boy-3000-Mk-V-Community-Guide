# how to open your Pip-boy safely and optionally replace your sd card (also manual reset)

Below is a guide to opening your device and accessing the sd card safely, if you have already done this please skip to the section on formatting your card and replacing the files. Make sure you feel confident to do this as there are several small wires that can be easily damaged. The Pip-boy will take and micro sd card thats correctly formatted but for stability its recommended to keep it below 32gb.

## Section 1: Preperation and opening the device

Step 1. Ensure you're ready to do this, you will need: a clear and well lit workspace, a small philips head screwdriver, a pair of needle nose pliers (optional).
![Photo of tools needed](https://github.com/user-attachments/assets/6a2337fd-fe8f-4cc3-af88-88a99baf9df6)

Step 2. Remove the foam cushioning from behind the screen and pry the edge of the black plastic with either your finger or the screwdriver to reveal the battery compartment. 
![Photo of cushion removed](https://github.com/user-attachments/assets/375d94ff-3150-4a33-87c2-e1eb165f19d8)

![Photo of removed plastic](https://github.com/user-attachments/assets/d60430ef-595c-45fa-a31a-34b0018259a9)

Step 3. Undo the battery compartment screw and remove the battery cover exposing the battery.

![photo of battery screw](https://github.com/user-attachments/assets/02bb2cbc-e5a6-4a24-b61a-a27af8d37bcc)
![photo of battery](https://github.com/user-attachments/assets/a70181c3-3ed8-446a-9204-2cdd28bb7cef)

Step 4. Remove the battery from its cutout and either using your fingers or the pliers VERY GENTLY pull out the battery pin. Only grip the pin by the two thinnest sides of the white plug and gently wiggle back and forth to ease the plug out. **Do not pull on the wires or squeese the plug too tightly with the pliers** (if you are only resetting the device from the troubleshooting section then skip to step 3 in section 3 after this)
![photo of removed battery](https://github.com/user-attachments/assets/53c1f548-bed7-4e05-aae4-6a9d2c2cefa7)
![batt removal 1](https://github.com/user-attachments/assets/d1b4dcf8-0acd-4789-b90f-4122e0efab31)
![batt removal 2](https://github.com/user-attachments/assets/03517fde-8083-4b6e-8ba5-503c2694f6ce)

Step 5. Once you have succesfully removed the battery you can set about opening the device. apply gentle pressure with one hand to the area marked in green while using the opposing hand to remove the four red highlighted screws. These are the four screws that hold the two parts of the main body together, the oressure ensure they drop pull apart suddenly and damage the wires.
![screw removal](https://github.com/user-attachments/assets/7a5d896b-ff3f-420d-8390-56a411ebf281)

Step 6. **Carefully** Lift the wrist section of the Pip-Boy slightly upwards and let it rest on the remaining cuff behind it as shown in the below pictures. Be extra careful of the wires highlighted and take note of the highlighted sd card slot.
![exposed board](https://github.com/user-attachments/assets/cd690eb3-90db-4a4b-9c0c-05c33e298f5b)
![exposed board highlighted](https://github.com/user-attachments/assets/737ce987-9467-40dc-a3e9-a7037e728e54)

Final step. Gently press in on the edge of the sd card to remove it. You should feel a click and it will pop out to be removed.
![exposed sd card](https://github.com/user-attachments/assets/a4559957-9989-4500-90ac-30a040e31c6d)


## Section 2: Formatting and replacing your sd card

Step 1. Plug the sd card into your computer and make a new folder called "pip-boy backup" in a place of your choice, then highlight all files on the sd card you just plugged in and copy them to the new folder exactly as they are. This is now your backup of the stock sd card OS. If you do not wish to restore your pip-boy to any previously saved version or replace the sd card you can skip to the end of this section and return the sd card to its slot on the main board, otherwise continue to follow this guide.

Step 2. Whether you are replacing the sd card with a larger one or resetting an already used card the first step is to reformat, this will wipe the card of all data so ensure you have backed up the cards contents first. Then load the card into a drive management tool of your choice and format it to the following specifications (note your software may only allow you to select the first option, this isnt ideal but should still work):

* Volume name: Pip-Boy
* format: FAT or FAT32 if the card is bigger than 4gb
* Cluster size: 32kb
* Boot selection: non bootable
* Partition scheme: MBR
* Target system: BIOS or UEFI

Once you have selected the above options and formatted the card you can move on to adding the files.

Step 3. Either extract a zip of the current os or copy files from a backup of the current os to your newly formatted card, it should match the image below unless the pip-boy was previously modded and you are aiming to retain the modifications, returning the sd card to its stock state will effectively count as a reset and wipe all non factory additions.
<img width="1554" height="928" alt="Screenshot - Finder15September2025@2x" src="https://github.com/user-attachments/assets/d473034e-1c0f-4a00-bc72-a87476be399b" />

Its also important to try and ensure the version of the OS you copy over matches the version you previously had installed. If you are upgrading or downgrading the OS version please ensure you follow the last secttions optional step to "reflash", for more information on this please check the guide section on the system flash.

Step 4. Once the files on the sd card match you can eject your card from your computer and reinsert it into the device. Ensure you click it into place so its fully seated within the board.

## Section 3: rebuilding the device

Step 1. Ensuring the sd card is returned very slowly put the two pieces of the body back together. Make sure they sit flush all the way around and none of the previously shown cables are pinched between the two pieces. Your first time this may take a couple of attempts but take your time and be gentle.
![seam check](https://github.com/user-attachments/assets/b1beb447-8980-4193-af48-096d52ce4d52)

Step 2. Once you have the two pieces back together place pressure where you did before (battery slot) and return the four screws that held the body ensuring not to overtighten.

Step 3. Take the battery and look at the plug at the end of the wire and the receptacle now exposed in the battery bay. Line up the notch with the corresponding slot and give the plug a firm push to re attach the battery (Note at this point the pip-boy will begin to boot)
![Battery pin](https://github.com/user-attachments/assets/22ed949f-5c1e-4fe8-949f-85ff3a6ad79a)
![battery pin2](https://github.com/user-attachments/assets/8ddac90c-2b6a-4084-8153-7c487ba2dda7)

