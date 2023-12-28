Hi,

DSU automation for installing GSI/system images
in xz,zip,img,md5 format with 2 examples upon receipt of the device guarantee.

About,
Dynamic System Updates (DSU)

Dynamic System Updates (DSU) is a system feature introduced in Android 10 that has the following:

    -Download a new GSI (or other Android system image) to your device.
    -Creates a new dynamic partition.
    -Loads loaded the downloaded GSI onto the new partition.
    -Start the GSI as a guest operating system on the device.

DSU also allows you to easily switch between the current system image and the GSI, so you can try out the system/GSI without risking corruption of the current system image.


DSU requirements

DSU is dependent on the Android Dynamic Partition feature and requires the GSIs to be signed by Google or your OEMs as a trusted system image. (CustomROM GSI/System Images can also be used with this procedure)

DSU is a feature of your device manufacturer. Check your device manufacturer's support page for availability. Google has enabled DSU on Pixel & integrated newer devices since Android 10 Beta 4.



Here I have written a few tools that bring the respective resource into the DSU format and then the installation
on the device starts.
To do this, simply copy the system image or GSI into the folder and start the respective application, making sure that
Device is connected via USB cable.
You can use xz,zip,md5,img System Images.
The fascinating thing about it is that it unlocks the bootloader but it is not flashed with custom files, so that remains
Guarantee received.
As an example I have attached Android 13 LineageOS with SuperSu and Google's Android 14 Beta GSI, both run perfectly,
This is the beginning of the installation of custom ROMs under warranty without ROOT rights or custom recovery.

DSU is an Android function that is hidden in the developer options, i.e. native.


What do i have to do?
#################


0# First of all, create a backup with SmartSwitch because the data will be deleted in the following step

1# It requires an open bootloader so that the GSI ROMs can start (warranty remains valid)
   -Enable developer options as follows
   -Phone information>>Software information
   -Type “Build version” 7 times in a row and confirm with the unlock code
   -Now open developer options under Settings
   -Activate the 2 functions (oem-unlock/bootloader-unlock), (usb debugging)
   -then turn off the cell phone and connect the USB cable to the PC/cell phone
   -Now start the download mode with VOL+ & VOL- & Power buttons
   -In download mode, press VOL+ until the next menu appears
   -now confirm with VOL+ and the bootloader is unlocked (ATTENTION DATA WILL BE DELETED)
   
2# Now set up the Android system again
   -Recover data with SmartSwitch
   -Re-enable developer option and enable “USB debugging”.

3# Now you can choose one of the applications to install your downloaded CustomROMs
   If the Allow USB Debugging notification appears, please allow it permanently
   and then press allow.
   Now start the application again and it works
   Now enter the unlock code when prompted for “Dynamic System Update”,
   The installation begins.
   
4# When the installation is complete, please look at the instructions.jpeg

5# Now you can switch between the 2 operating systems as often as you want.





GSI CustomROM Sources

AndyYans GSI
https://sourceforge.net/projects/andyyan-gsi/files/

Sourceforge.net GSIs
https://sourceforge.net/directory/gsis/windows/

Generic System Image list
https://github.com/phhusson/treble_experimentations/wiki/Generic-System-Image-%28GSI%29-list

Google Android GSI
https://developer.android.com/topic/generic-system-image/releases

Samsung STOCKROM Firmware Website
https://samfw.com/

phhusson GSI list
https://magiskzip.com/gsi-list-phhusson/

Android ROM list
https://github.com/musabcel/android_rom_list