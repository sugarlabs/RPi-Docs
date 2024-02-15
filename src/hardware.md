### Installing Display Management System:

1. **Install Xorg Display Server**:
   - Open a terminal and run the following command to install the Xorg display server:
     ```bash
     sudo apt install xserver-xorg
     ```

2. **Install LightDM Display Manager**:
   - Run the following command to install the LightDM display manager:
     ```bash
     sudo apt install lightdm
     ```

3. **Set LightDM as Default Display Manager**:
   - Run the following command to set LightDM as the default display manager:
     ```bash
     sudo dpkg-reconfigure lightdm
     ```
   - Select "lightdm" from the list of display managers and press Enter.

4. **Reboot**:
   - Reboot your Raspberry Pi to apply the changes:
     ```bash
     sudo reboot
     ```

### Selecting Sugar as Desktop Environment:

1. **Install Sugar Desktop Environment**:
   - Open a terminal and run the following command to install the Sugar desktop environment:
     ```bash
     sudo apt install sucrose
     ```

2. **Configure Sugar as Default Desktop Environment**:
   - Run the following command to configure Sugar as the default desktop environment:
     ```bash
     sudo update-alternatives --config x-session-manager
     ```
3. **Reboot**:
   - Reboot your Raspberry Pi to apply the changes:
     ```bash
     sudo reboot
     ```
    - In the Display management GUI , Select "sugar" from the list and press Enter.

### [Starting with Development](https://github.com/sugarlabs/sugar/blob/master/docs/development-environment.md)
   
   - Start developing Sugar and its components according to your requirements you can see the given link for more info.
