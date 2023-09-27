# How to Format USB Flash Drive from Command Prompt

This page mainly illustrates how to format a USB flash drive using Windows inbuilt Command Prompt, and the following is the detailed guide you should strictly follow.

## Step 1: Open Command Prompt as Administrator

1. Type `cmd` in the search box.
2. Right-click on the `Command Prompt` app and select `Run as administrator`.

## Step 2: List Disks

1. In the Command Prompt window, type `diskpart` and press `Enter`.
2. Type `list disk` and press `Enter`.
3. This will list all the disks that are connected to your computer.

## Step 3: Select the USB Flash Drive

1. Find the disk number of your USB flash drive in the list.
2. Type `select disk [disk number]` and press `Enter`.

## Step 4: Clean the USB Flash Drive

1. Type `clean` and press `Enter`.
2. This will erase all the data on your USB flash drive.

## Step 5: Create a Partition

1. Type `create partition primary` and press `Enter`.
2. This will create a new partition on your USB flash drive.

## Step 6: Format the USB Flash Drive

1. Type `format fs=ntfs quick` and press `Enter`.
2. This will format the USB flash drive with the NTFS file system.

## Step 7: Exit Diskpart

1. Type `exit` and press `Enter`.
2. This will exit the Diskpart utility.

## Congratulations!

Your USB flash drive has now been formatted. You can now use it to store files.
