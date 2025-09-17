# File Types and Formatting

## Introduction

Your wand company Pip-boy uses two primary file types to cover the vast majority of media. Video files are AVI while audio typically uses WAV. By creating files in these two specific formats we can add or replace files within the pip-boy, for example we can replace the audio files in the radio folder with our own custom files, allowing us to add our own music without using the custom radio app. We can also add custom AVI files to play in certain tabs including the maps section. In this guide will be a breakdown of each of these two file types and tools you can use to both convert and upload the files to your device.

## Formats

### **Video:** AVI file set at 12fps with an aspect ratio of 408x248px
### **Audio:** WAV file in 16bit Mono

## Community Converter (Windows)
### We have a premade .exe tool based on FFMPEG created by @codytolene right [here](https://github.com/CodyTolene/pip-boy-3000-mk-v-media-converter.git) on github. The application can be installed and used by following the instructions on its repository. Alternatively you can follow the guide below to download FFMPEG directly and use it in your shell (terminal)

## FFMPEG (All Platforms)

### [Install Guide Windows](https://phoenixnap.com/kb/ffmpeg-windows)
### [Install Guide Mac](https://phoenixnap.com/kb/ffmpeg-windows)
### [Install Guide Ubuntu](https://phoenixnap.com/kb/install-ffmpeg-ubuntu)

### FFMPEG Commands for pip-boy video and audio:
#### Audio = "ffmpeg -i X -ac 1 -ar 16000  X"
#### Video = "fmpeg -i X -vf "scale=400:-1,format=rgb555le" -r 12 -c:v msrle -pix_fmt pal8 -c:a pcm_s16le -ac 1 -ar 11025 X"

#### Once You have FFMPEG installed follow the next steps to convert a file

#### Step 1: Open a folder with the file you want to convert, a terminal window and a notepad or any writing applications window with the command you want pasted into it. This process works the same for both audio and video you just switch which command to paste. Take note how things are laid out below and the position of the X's as that will be important in a second.

<img width="1427" height="596" alt="Screenshot - Terminal16September2025@2x" src="https://github.com/user-attachments/assets/c54ba22a-7ab6-45d0-84b7-72552dde96d7" />

#### Step 2. Drag the file from your folder and drop it in to your terminal to get the exact file path for the file you want to convert. It should look something like "/Users/theghoul/downloads/my_funny_video.mp4"

<img width="1427" height="596" alt="Screenshot - Terminal16September2025 2@2x" src="https://github.com/user-attachments/assets/d71e4b50-9374-4673-8b24-0c4eb55efa60" />

#### Step 3. Copy the file path from the terminal and replace the two highlighted X's with it. The first should be copied to where the first x is exactly **However** the second should be adjusted so instead of ".mp4" or ".m4a" it says ".avi". It should look something like this: "ffmpeg -i /Users/theghoul/downloads/my_funny_video.mp4 -vf "scale=400:-1,format=rgb555le" -r 12 -c:v msrle -pix_fmt pal8 -c:a pcm_s16le -ac 1 -ar 11025 /Users/theghoul/downloads/my_funny_video.avi"

<img width="1427" height="596" alt="Screenshot - Terminal16September2025 3@2x" src="https://github.com/user-attachments/assets/c5819930-2939-407f-a37b-c1dba50d4c46" />

#### Final step: Copy the prewritten command to your terminal and run it, once converted the new file will be placed next to the original and be ready for upload in the next section.

## File Locations and Uploading

#### Now we have our file its time to decide where to place it, You can either drop it into a pre-existing folder on your device like "misc" in which thr file will show in the STATS section of the DATA tab or you can create a new directory on your device and view the file with the file explorer app. For the sake of this guide ill be adding a short video to the misc section so it shows up in the UI. Note that larger files should be added manually onto the sd card itself to prevent issues.

<img width="1675" height="1020" alt="Screenshot - Google Chrome16September2025@2x" src="https://github.com/user-attachments/assets/94639ba9-026f-40eb-a094-ce2276390985" />
Navigate to this website and coonnect your device

<img width="1675" height="1020" alt="Screenshot - Google Chrome16September2025 2@2x" src="https://github.com/user-attachments/assets/2988795a-53a0-476d-9ed8-cd71e5899163" />
Once connected scroll down to where it says "load files" and select the file or files you want to upload

<img width="1675" height="1020" alt="Screenshot - Google Chrome16September2025 3@2x" src="https://github.com/user-attachments/assets/5f804936-86ab-48f2-9eda-800273dea52a" />
You can now select which sub directory you wish to add the files to or you can create a new folder

<img width="1675" height="1020" alt="Screenshot - Google Chrome16September2025@2x copy" src="https://github.com/user-attachments/assets/ea0b7d95-b53e-4718-902b-835b6f9b28b3" />
Once you click "start upload"the site will add the file to the directory (this may take a while for larger files) and then you will be done and can view your files in the device. 

## Deleting files

#### To delete files you can use the file browser on the same window and click the trash icon next to any file you no longer want. I would strongly advise against deleting files youre unsure of as you can cause issues. For details on removing audio files to replace them within the radio please see the Custom radio portion of the guide.

