# IAZ
Integrated ROM Source Based App Zipper

This is an Integrated Shell Script based Solution/Template to compile apps from ROM source & Zip them Automatically.<br>
The Scripts Use DEVICE_MODEL variable to setup the Environment & compile apps.<br>

# Setup
- Add the following line to your manifest: <br>
<code>\<project name="nutcasev15/IAZ" path="tools/IAZ" remote="github" revision="Template" /\></code><br>
- Customize the Updater-Binary, Device Model Info & Lunch/Breakfast support in the IAZ Script
- Add a Predefined List of Apps to Compile in IAZ Script
- Commit Changes
- Run the following command in ROM Src root:<br>
<code>./tools/IAZ/IAZ</code>
- A Flashable Zip Should be Created in the ROM's Parent Directory.

# Compiling A Given Set Of Apps
  Refer the IAZ Script in Template Branch & Z00A_lineage Branch.
  
# Zipping Precompiled Apps
  - Complete Compiling the Apps
  - Run the command in ROM Src root:<br>
   <code>export PONLY=true</code>
  - Run IAZ Script.
  
# FAQ

- My Zip Fails to Flash. What Shall I Do?<br>
>This is probably because the included updater-binary is for x86 based phones. Replace & Retry.<br><br>
- Where is the ZIP created?<br>
>It created in the parent of the ROM Src Directory.<br><br>
- The Script gives me "cannot stat \<insert path here\>" errors. What next?<br>
>The script is designed to be run from the root of the ROM Src, while the this repo is cloned under "tools/IAZ" directory of the Src.<br><br>
- What is Src?<br>
>Not My Problem ;)
