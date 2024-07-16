# Package Installation Guide

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

## 6. Overall Flow

![htmlCode_page-0001](https://github.com/user-attachments/assets/314ced33-04f7-4e0d-b504-53c7f11b3023)



