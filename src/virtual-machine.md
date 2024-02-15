### Setting up Raspberry Pi in VirtualBox (Windows):

1. **Download Raspberry Pi OS Lite Image**: 
   - Visit the [official Raspberry Pi website](https://www.raspberrypi.org/software/operating-systems/) and download the Raspberry Pi OS image.

2. **Install VirtualBox**: 
   - Download and install VirtualBox from the [official VirtualBox website](https://www.virtualbox.org/).

3. **Create a New Virtual Machine**: 
   - Open VirtualBox and click on "New" to create a new virtual machine.
   - Choose a name for the virtual machine and select "Linux" as the type, and "Other Linux (64-bit)" as the version.
   - Allocate memory and create a virtual hard disk.

4. **Configure Virtual Machine Settings**: 
   - Select the newly created virtual machine and click on "Settings".
   - Under "System", change the boot order to boot from the virtual optical disk.
   - Under "Storage", add the Raspberry Pi OS Lite image as the optical disk.

5. **Boot and Install Raspberry Pi OS**: 
   - Start the virtual machine and follow the on-screen prompts to install Raspberry Pi OS.

6. **Install Sugar Desktop Environment**: 
   - Once Raspberry Pi OS is installed, open a terminal and run:
     ```bash
     sudo apt update
     sudo apt install sucrose
     ```

7. **Configure Sugar as Default Desktop Environment**: 
   - Run the command:
     ```bash
     sudo update-alternatives --config x-session-manager
     ```
   - Select Sugar from the list and press Enter.

8. **Reboot and Start Sugar**: 
   - Reboot the virtual machine and Sugar should start automatically.

### Setting up Raspberry Pi in VMware (Windows and macOS):

The process is similar to VirtualBox but with slight variations in VMware. Follow steps 1 to 7 from the VirtualBox guide, then continue with the following:

9. **Install VMware Tools (Optional)**:
   - In VMware, go to "Virtual Machine" > "Install VMware Tools" to mount the VMware Tools ISO.
   - Follow the on-screen instructions to install VMware Tools for better integration and performance.

### Setting up Raspberry Pi in QEMU (macOS):

1. **Install QEMU**:
   - Install QEMU on macOS using Homebrew:
     ```bash
     brew install qemu
     ```

2. **Download Raspberry Pi OS Lite Image**: 
   - Download the Raspberry Pi OS Lite image from the official Raspberry Pi website.

3. **Create QEMU Virtual Machine**: 
   - Run the following command in the terminal to create a QEMU virtual machine:
     ```bash
     qemu-img create -f qcow2 raspbian_lite.img 4G
     ```
    - or any other image of your choice can be downloaded just keep the name and path correct.

4. **Run QEMU**: 
   - Start the virtual machine with the following command:
     ```bash
     qemu-system-arm -m 512M -M versatilepb -cpu arm1176 -kernel kernel-qemu-4.19.50-buster -append "root=/dev/sda2 rootfstype=ext4 rw" -drive "file=raspbian_lite.img,format=qcow2" -net nic -net user,hostfwd=tcp::5022-:22 -no-reboot -display none -serial stdio
     ```
    - This is not supposed to be exactly copy pasted but should act as a guide as you might need to change the folder address at will.

5. **Install Sugar Desktop Environment**: 
   - Once Raspberry Pi OS is installed in QEMU, open a terminal and run:
     ```bash
     sudo apt update
     sudo apt install sucrose
     ```

6. **Configure Sugar as Default Desktop Environment**: 
   - Follow steps 7 and 8 from the VirtualBox guide.

### Setting up Raspberry Pi in UTM (macOS):
(This is best suited and adviced for mac users)

1. **Install UTM from the App Store**:
   - UTM is available for download from the macOS App Store.

2. **Create New Virtual Machine**:
   - Open UTM and create a new virtual machine.
   - Choose "Linux" as the guest operating system and select the Raspberry Pi OS Lite image.

3. **Start Virtual Machine and Install Raspberry Pi OS**:
   - Start the virtual machine and follow the on-screen prompts to install Raspberry Pi OS Lite.

4. **Install Sugar Desktop Environment**: 
   - Once Raspberry Pi OS is installed in UTM, open a terminal and run:
     ```bash
     sudo apt update
     sudo apt install sucrose
     ```

5. **Configure Sugar as Default Desktop Environment**: 
   - Follow steps 7 and 8 from the VirtualBox guide.
