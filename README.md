# Config_my_laptop_Ubuntu_18.04
This repository is for installing NVIDIA driver and other related drivers (bluetooth and etc.) to install on Ubuntu 18.04 LTS

## Bluetooth

If you're experiencing Bluetooth issues on Ubuntu, you can try the following steps:

1. Install the `pulseaudio-module-bluetooth` package:

    ```bash
    sudo apt-get install pulseaudio-module-bluetooth
    ```

2. Restart the PulseAudio service:

    ```bash
    sudo killall pulseaudio
    pulseaudio --start
    ```

3. Restart the Bluetooth service:

    ```bash
    sudo systemctl restart bluetooth
    ```

4. Turn off and on your Bluetooth from your system settings, then reconnect your devices.

## NVIDIA Driver

Installing the NVIDIA driver on Ubuntu may require some manual steps. Here's a guide to help you through the process:

1. **Preparation**:
   - Before installing the NVIDIA driver, ensure your system is up to date:

     ```bash
     sudo apt update
     sudo apt upgrade
     ```

   - Install some essential packages:

     ```bash
     sudo apt -y install cmake cmake-gui zsh snap vim htop terminator gimp gawk build-essential dkms ccze
     sudo snap install ttyplot
     ```

2. **Installing NVIDIA Driver**:
   - Follow this [video tutorial](https://youtube.com/watch?v=GljujCLixzE&t=569s) for step-by-step instructions on installing the NVIDIA driver.

   - Make sure to double-check the associated [GitHub link](https://gist.github.com/hangsong/c0c3839ebfea7b683287db539785bc10) provided in the video for additional information.

3. **Troubleshooting**:
   - If you encounter any issues with your black display, you can try the following:
     - Press `CTRL + ALT + (F1 or F2 or F3 or F4 or F5 or F6)` to access the lock screen or TTY.
     - Login into your account
     - Adjust your GRUB settings, adding or removing `nomodeset`.
     - Update GRUB and reboot your system.

   - If all else fails, consider uninstalling the NVIDIA driver and reinstalling it.

That's it! If you successfully install the NVIDIA driver, please let me know. 🚀
