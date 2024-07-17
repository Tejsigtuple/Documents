<div align="center">
   
   # Package Installation Guide
</div>

<br>

# Phase I

## 1. Introduction

This guide provides step-by-step instructions for installing the nila_compose package from the GitHub repository. The process involves setting up the environment, downloading necessary files, and configuring the application.

## 2. Prerequisites

- A GitHub account
- Access to the "nila_compose" repository
- Administrative privileges on your local machine
- Basic familiarity with terminal/command line operations

## 3. Installation Steps

### 3.1 Access GitHub Repository

1. Open any web browser and navigate to GitHub.
2. Locate the "nila_compose" repository.
3. Switch to the "horeba_rc_1" branch.

### 3.2 Set Up Initial Script

1. Find the "setup.sh" file in the "horeba_rc_1" branch.
2. Copy the entire content of "setup.sh".
3. Open your terminal application.
4. Create and edit the setup.sh file with elevated privileges:
   ```
   sudo nano setup.sh
   ```
5. Paste the copied content into the nano editor.
6. Save the file (Ctrl + O, then Enter) and exit nano (Ctrl + X).
7. Execute the setup script:
   ```
   sudo bash setup.sh
   ```
8. Download the setup files from GitHub to your local machine.
9. Navigate to the nila_compose directory:
   ```
   cd nila_compose
   ```
10. Run the prepare_device.sh script:
   ```
   sudo bash prepare_device.sh
   ```

### 3.4 Launch and Configure the Application

1. Launch the application:
   ```
   bash scripts/launch_app.sh
   ```
2. Enter the required details when prompted (device name, password, email).
3. Exit the application by pressing Ctrl + C.

### 3.5 Finalize Installation

1. Reboot the system:
   ```
   sudo reboot
   ```

## 4. Troubleshooting

If you encounter any issues during the installation process:

- Ensure you have the necessary permissions to execute the scripts.
- Check your internet connection if you're having trouble accessing GitHub or downloading files.
- Verify that all prerequisites are met before starting the installation.
- If a script fails, try running it again with verbose output.

## 5. Conclusion

After completing these steps, the nila_compose application should be installed and configured on your system. It will launch automatically after rebooting, tailored specifically for your user account without requiring system-wide changes or additional service management configurations.

For further assistance or questions, please contact the support team.

## 6. Phase I Overall Flow

![htmlCode_page-0001](https://github.com/user-attachments/assets/314ced33-04f7-4e0d-b504-53c7f11b3023)

# Phase II

## 7. Pylon Installation

- Visit the Basler website to download the Pylon Camera Software Suite for Linux.
- The URL is usually something like Basler Pylon Download.
- Select the appropriate version of the Pylon package for your system (e.g., 64-bit Debian package).
- Download the ".deb" file to your system. For example, the file might be named pylon_6.2.0.21469-deb0_amd64.deb.
- Open your terminal. Change directory to where the ".deb" file is downloaded. For example:
   ```
   sudo ~/Downloads
   ```
-  Use "dpkg" to install the Pylon package:
   ```
   sudo dpkg -i pylon_6.2.0.21469-deb0_amd64.deb
   ```
- If there are any missing dependencies, fix them using:
   ```
   sudo apt-get install -f
   ```
- Check if the installation was successful by listing the installed pylon packages:
   ```
   dpkg -l | grep pylon
   ```
- It is recommended to reboot your system after installation to ensure all settings take effect:
   ```
   sudo reboot
   ```
### Additional Notes
- Ensure you have downloaded the correct version of the Pylon software that matches your operating system's architecture (e.g., 64-bit).
- After installation, you can use the Pylon Viewer and other tools provided by the Pylon Camera Software Suite to interface with your Basler camera.

## 8. Import files from other device

### 8.1 Steps to Connect to a Device
1. Open your terminal application.
2. Use the following SSH command to connect to the remote device. Replace user with the appropriate username and 192.168.1.xxx with the IP address of the remote device.
   ```
   ssh user@192.168.1.100
   ```
### Copy the Folder to Your Local Machine
1. Once connected, navigate to the sigtuple_dev folder located in the Desktop directory. Use the following command:
   ```
   cd ~/Desktop/sigtuple_dev
   ```
2. Copy the full path of the sigtuple_dev folder for later use. You can use the pwd command to print the working directory path:
   ```
   pwd
   ```
3. After copying the path, exit the SSH session by typing:
   ```
   exit
   ```
4. Use the 'scp' command to copy the entire 'sigtuple_dev' folder from the remote device to your local machine. Replace 'user' with the appropriate username, '192.168.1.100' with the IP address of the remote device, and adjust the destination path as necessary.
   ```
   scp -r user@192.168.1.100:~/Desktop/sigtuple_dev ~/local_destination_path
   ```
5. This command recursively copies the 'sigtuple_dev' folder from the remote device to the specified directory on your local machine (~/local_destination_path).
## 9.0 To Establish the Connection between Hardware & Local Machine
### 9.1 List Connected Ports:
1. Open your terminal application.
2. Use the 'ls' command with 'grep' to find ports.
   ```
   ls /dev | grep ttyAC
   ```
3. This will list all devices connected to ports that match ttyAC.
### 9.2 Set Permissions:
5. Set read and write permissions using 'chmod':
   ```
   sudo chmod 666 /dev/ttyACM*
   ```
6. This command sets the permission of all devices matching ttyACM* to be readable and writable by all users.
### 9.3 Navigate to the SigtupleDev Directory:
1. Change to your project directory where your virtual environment and script are located.
2. Use the Python interpreter from your virtual environment to run the script:
   ```
   .venv/bin/python leapapp.py
   ```
3. Once the leapapp.py script is running, you will be able to control the device via the LeapApp console.






