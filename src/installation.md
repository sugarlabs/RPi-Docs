# Installation Guide for Sugar on Raspberry Pi

Follow these steps to install Sugar on Raspberry Pi:

## Step 1: Download Raspberry Pi OS Lite Image

Download the latest Raspberry Pi OS Lite image from the official [Raspberry](https://www.raspberrypi.com/) Pi website.

## Step 2: Flash Image to MicroSD Card

You can use Raspberry app interface and select desired models to be flashed.

## Step 3: Boot Raspberry Pi

Insert the microSD card into your Raspberry Pi and power it on. Follow the on-screen prompts to set up the Raspberry Pi OS.

## Step 4: Update System Packages

Once Raspberry Pi OS is up, update the system packages:

```bash
sudo apt update
```
```bash
sudo apt upgrade
```

## Step 5: Install Sugar Desktop Environment

Run the following commands to install the Sugar desktop environment:

```bash
sudo apt install sucrose
```

## Step 6: Configure Sugar

Configure Sugar as the default desktop environment:

```bash
sudo update-alternatives --config x-session-manager
```

Select Sugar from the list and press Enter.

## Step 7: Reboot Raspberry Pi

```bash
sudo reboot
```

## Step 8: Launched Sugar


After rebooting the Raspberry Pi, Sugar should start automatically. Remember to verify whether the Sugar Desktop Environment is installed and to disable auto-login in the RPi-config settings. If you encounter any difficulties, you may need to proceed with troubleshooting