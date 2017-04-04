<ol>
<p><li> Put the Devo transmitter in flash mode by holding down the EXT button while turning on the power.

<p><li> Connect the transmitter to you computer with a USB cable.

<p><li> Double-click the jar file, then click the DFU tab and upload the .dfu file in the folder. 

<p><li> Once the firmware is flashed, turn the transmitter off, then turn it back on with the ENT button held down.
You should get a big USB symbol on the LCD display.

<p><li> In a terminal window, enter the command

  fdisk /dev/sdb

Select 'n' to create a new partition. Select 'Primary' type, and the default start and end cylinders. Enter 'w' to write the new partition and exit fdisk. Be careful!!! If you accidentally use fdisk on some other disk device you could wipe your Linux drives! (you were warned)

<p><li> Enter the command 

  mkfs -t vfat /dev/sdb1

A new disk image will appear on your desktop.

<p><li> Copy the contents of the folder into this new disk.  Power-cycle your transmitter, and you should see the Deviation splash screen.
</ol>
