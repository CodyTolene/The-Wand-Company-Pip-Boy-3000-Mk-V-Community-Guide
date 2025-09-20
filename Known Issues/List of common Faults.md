# List of Common Faults

## Apps fail to load, UI slow and sluggish, Delayed sound
The device ships with very limited RAM and so its to be expected that at times it may slow down or struggle to process big tasks, Especially with long uptimes. This is usually fixed just by regularly rebooting the device, Most of our apps now include a mini reboot both at opening nd closing to help ensure this issue isnt persistent.

## Battery Indicator Innacurate
This is less of a bug and moe just a limitation of how the circuit gauges the battery level. Currently there is no fix and its just a quirk we have to live with.

## Sd Card Space not Updating on Maintenance Tab of Pip-boy Website
This is another known issue and a limit to the current system. If you delete files until the sd card has been reformatted or other edits are made the sd card may not show as space having been freed.

## Apps Fail to Download/Install
Sometimes the app loader has trouble installignapps to your device. This can be due to a myriad of circumstances too long to list here. The best practice is to try again and if you experience any further problems with the device not behaving as normal after you should follow the troubleshooting steps [here](https://github.com/beaverboy-12/The-Wand-Company-Pip-Boy-3000-Mk-V-Community-Guide/blob/main/Individual%20Guides/Basic%20device%20Info%20and%20Troubleshooting.md). If after three attempts the app still wont install then try to reach out on the community discord for support.

## The Wand Company Erase link Cant Complete
Its a known issue (hopefully soon patched) that non stock sd cards can fail during the erase function using the official tool. This ultimately means its safer to avoid the erase link if you have upgraded your sd card and instead manually modify or reset your firmware as laid out [Here](https://github.com/beaverboy-12/The-Wand-Company-Pip-Boy-3000-Mk-V-Community-Guide/blob/main/Individual%20Guides/Deconstruction%20and%20Sd%20card%20Replacement.md). If you still hae the stock card installed and you face this issue you should follow the troubleshooting steps hosted [here](https://github.com/beaverboy-12/The-Wand-Company-Pip-Boy-3000-Mk-V-Community-Guide/blob/main/Individual%20Guides/Basic%20device%20Info%20and%20Troubleshooting.md) and seek further help in the discord if you still have no luck.

## Failure to Connect to the Computer
Failure to connect can be caused by a myriad of things. Before we assume theres a definitive problem theres a few things to check first:
* Check you're using a browser that supports web serial like chrome
* Check you have no other tabs open with an active connection to the device (for example failing to connect to the maintenance page while still connected to the app installer)
* Ensure the device is turned on
* Reboot the device by going to DATA>MAINTENANCE>REBOOT
* Check the cable is correctly seated both in the computers port and the Pip-boys cable port
* Try a differenct cable to rule out problems with that specific one (even if the cable allows the device to charge it may still be damaged to prevent data transfer)
If after checking these things you still have no luck the next step will be to reach out to the community discord for further troubleshooting. You can find the link on the index page of this repository.

## Broken Screens
There is a know issue where trying to remove the motherboard of your device causes a particular component to crack the lcd screen. To avoid this you should be extra careful always when trying to remove any components beyony the sd card. 
In the instance that you break your screen this way or any other way you should contact the wand company for repair or replacement [here](https://www.thewandcompany.com/contact-us/)
![WhatsApp_Image_2025-08-28_at_22 41 25_d80598ed - 01](https://github.com/user-attachments/assets/de82e176-488b-4299-b7b9-145e18097008)![rn_image_picker_lib_temp_afa592e2-eb71-4666-8323-f91775156b89 - 01 - 01](https://github.com/user-attachments/assets/652ec857-07d1-4f61-a19c-23b38c1402e5)

## Screen Blank/ No picture (sound still functioning, rad meter light on)
Sometimes the screen can fail to light if the pip-boy hasnt been rebooted in a while or if theres a small bug etc. Most of the time it can be fixed following the steps provided in the [troubleshooting](https://github.com/beaverboy-12/The-Wand-Company-Pip-Boy-3000-Mk-V-Community-Guide/blob/main/Individual%20Guides/Basic%20device%20Info%20and%20Troubleshooting.md) section. 

## Screen Blank/ No picture (no sound, rad meter unlit)
If the screen is blank and there is also no sound or lights on the rad meter then there may be a larger issue. To check the screen functions you can use the "Factory test" or "demo" function withtin the maintenance tab of the [Pip-boy](https://pip-boy.com/3000-mk-v/maintenance) website. If the problem persists and normal [troubleshooting](https://github.com/beaverboy-12/The-Wand-Company-Pip-Boy-3000-Mk-V-Community-Guide/blob/main/Individual%20Guides/Basic%20device%20Info%20and%20Troubleshooting.md) doesnt work then please follow the link [here](https://www.thewandcompany.com/contact-us/) to contact the manufacturer for futher help.
