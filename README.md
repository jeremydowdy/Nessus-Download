# Nessus-Download

**For Windows**
How to download Tenable Nessus
Nessus Installation
Select Nessus Version:
Choose the version of Nessus that suits your needs (e.g., Nessus Professional, Nessus Home, etc.).

Create an Account
In most cases, you will need to create an account on the Tenable website or log in if you already have one.

Download Nessus
Once you have an account and are logged in, navigate to the download section and choose the appropriate version for the system you wish to install it to.

Select the Platform:
Choose the platform for which you want to download Nessus. Make sure to download the correct version based on your system architecture.

Download the Installer:
Click on the download link to initiate the download of the Nessus installer.

Run the Installer:
Once the download is complete, run the installer executable (.exe file for windows) that you downloaded. Follow the on-screen instructions to install Nessus on your system.

Set Up Nessus:
During the installation process, you may be prompted to configure settings and set up your Nessus account. Follow the prompts to complete the setup. SAVE YOUR ACTIVATION KEY TO NOTEPAD FOR FUTURE REFRENCE

Activate Nessus:
After installation, you may need to activate Nessus using the license or activation key provided by Tenable druing setup in your browser. You will be prompted that the website isnt safe, go into advanced and continue to the site to complete setup. Follow the activation process to complete the setup. Initilization will take some time. For computers with low end processing power and memory, it would be best practice to run the initialization in the browser and have no other programs running until it completes to prevent thermal throttling and excessive wear on your components.

Access Nessus Web Interface:
Once installed and activated, you can access Nessus through a web browser by entering the provided URL (usually https://localhost:8834).

Remember to refer to the official Tenable documentation or support resources for any specific details or updates related to Nessus installation.

# **For Linux**
**Download Nessus using curl**

1. **Visit the Nessus Download Page:**
   Go to the [official Tenable Nessus download page](https://www.tenable.com/downloads/nessus) to get the URL for the version you want.

2. **Right-click on the Download Button:**
   On the Nessus download page, right-click on the download button for the version you want and copy the link address.

3. **Use `curl` Command:**
   Open your terminal or command prompt and use the following `curl` command to download Nessus.

   Replace `<download_link>` with the actual link you copied.

   ```bash
   curl -o Nessus.tar.gz <download_link>

   
## Installing Nessus on Kali Linux

1. **Register for Nessus:**
   - Go to the [Tenable website](https://www.tenable.com/), register for an account, and obtain a license for Nessus.

2. **Download Nessus:**
   - Once registered and logged in, navigate to the download section and download the appropriate package for your operating system. For Kali Linux, you might look for a Debian or Ubuntu package.

3. **Install Nessus:**
   - Use the appropriate package manager to install Nessus. For Debian-based systems like Kali Linux, you would use the `dpkg` package manager.
     ```bash
     sudo dpkg -i Nessus-<version>-debian6_amd64.deb
     ```
     Replace `<version>` with the actual version number of the Nessus package you downloaded.

4. **Start Nessus:**
   - Start the Nessus service with the following command:
     ```bash
     sudo service nessusd start
     ```

5. **Access Nessus Web Interface:**
   - Open a web browser and navigate to [https://localhost:8834](https://localhost:8834). Follow the on-screen instructions to set up Nessus, including creating an admin user and activating the license.

Please note that the steps might vary slightly depending on the specific version of Nessus and Kali Linux that you are using. Additionally, Tenable's policies may change, so it's a good idea to check their official documentation for the most up-to-date information.


# REMOVING NESSUS

**For Windows:**

If your control panel is organized by category:

Select uninstall a program
Find the Nessus program
Click Uninstall
**you may receive a pop up showing unistall progress, if that stalls, open task manager and expand the User Account Control (UAC) program shown and give it permission to make changes to your disc to allow the uninstall to complete**

If you view control panel in small icons:

Go to programs and features
Select Nessus and unisntall
If you have issues unisntalling view bold and italicized statement above

# Removing Nessus from Linux

## Uninstalling Nessus from Linux

The exact command to uninstall Nessus from Linux can depend on how Nessus was installed and which package manager your Linux distribution uses. Assuming you installed Nessus using a package manager like dpkg (common in Debian-based systems like Ubuntu) or rpm (common in Red Hat-based systems like Fedora), here are general steps:

### Debian/Ubuntu-based Systems:
If Nessus was installed using dpkg, you can use the dpkg command to uninstall it. Open a terminal and run:

```bash
sudo dpkg -r nessus
```

If that doesnt work you can run

```bash
sudo apt-get remove --purge nessus
```
Remember to run these commands with sudo to ensure you have the necessary permissions to uninstall the software. Also, please refer to the Nessus documentation or the specific instructions provided by Tenable, the company behind Nessus, for any special uninstallation procedures related to your specific installation.

The exact command to uninstall Nessus from Linux can depend on how Nessus was installed and which package manager your Linux distribution uses. Assuming you installed Nessus using a package manager like dpkg (common in Debian-based systems like Ubuntu) or rpm (common in Red Hat-based systems like Fedora), here are general steps:

Red Hat/Fedora-based Systems:
If Nessus was installed using rpm, you can use the rpm command to uninstall it. Open a terminal and run:

```bash
sudo rpm -e nessus
```
General Method:
If you're unsure or the above commands don't work, you can try to locate the Nessus package name and then remove it. Use the following commands:

For Debian/Ubuntu-based systems

```bash
sudo apt-get remove --purge $(dpkg -l | grep nessus | awk '{print $2}')
```

For Red Hat/Fedora-based systems

```bash
sudo yum remove nessus
```

Make sure to replace "nessus" with the actual package name if it's different.

Remember to run these commands with sudo to ensure you have the necessary permissions to uninstall the software. Also, please refer to the Nessus documentation or the specific instructions provided by Tenable, the company behind Nessus, for any special uninstallation procedures related to your specific installation.


