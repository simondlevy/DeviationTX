I love the Deviation firmware for Walkera Devo7E transmitter, but I was frustrated trying to locate the software tools
and files needed to put the firmware on my transmitters. So I collected these
tools and files into a single repository, which has everything you need to
flash the firmware onto your Devo7E on Windows and Linux.

First, you'll need Java on your computer. To see whether it's there, double-click on <b>DeviationUpload-0.8.0.jar</b>.
If a little dialog window pops up, you're set.  Otherwise, <a href="https://java.com/en/">download</a> and install 
Java now.  Then follow these directions:

<ol>
<p><li> Put the Devo transmitter in flash mode by holding down the EXT button while turning on the power.

<p><li> Connect the transmitter to you computer with a USB cable.

<p><li> Double-click the jar file, then click the <b>DFU</b> tab and then the <b>...</b> upload button.  Navigate to 
the <b>devo7e</b> folder in this repository, and select the .dfu file.  Click <b>Send</b> to flash the firmware onto
your Devo7E transmitter.

<p><li> Once the firmware is flashed, turn the transmitter off, then turn it back on with the ENT button held down.
You should get a big USB symbol on the LCD display.
</ol>

What you do next depends on your operating system.  

<h2>Windows</h2>

<ol>
<li>In <b>My Computer</b> or <b>File Explorer</b> you should see an <b>E:</b> drive, or other new drive that
wasn't there before. Right-click on this drive to format it, using the default format settings.  
<b> Be sure you've selected the correct drive, so you don't reformat an existing drive an lose all your data</b>
<p><li>Copy the contents of the <b>devo7e\filesystem</b> folder into the newly-formatted drive.
</ol>

<h2>Linux</h2>

<ol>

<p><li> In a terminal window, enter the command

  fdisk /dev/sdb

Select 'n' to create a new partition. Select 'Primary' type, and the default
start and end cylinders. Enter 'w' to write the new partition and exit fdisk.
<b>Be careful!!! If you accidentally use fdisk on some other disk device you
could wipe your Linux drives! (you were warned)</b>

<p><li> Enter the command 

  mkfs -t vfat /dev/sdb1

A new disk image will appear on your desktop.

<p><li> Copy the contents of the folder into this new disk.  
</ol>


Power-cycle your transmitter, and you should see the Deviation splash screen.
