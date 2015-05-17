**timelinex_acpi** - simple kernel module that disables ATI discrete VGA-card.

----
## Installation

    make
    sudo make install
    echo timelinex_acpi | sudo tee -a /etc/modules > /dev/null
Deny Radeon module to start with

    echo "blacklist radeon" | sudo tee -a /etc/modprobe.d/blacklist.conf > /dev/null

After reboot your Radeon is deactivated.

----
## TLP
see [Documentation](https://launchpad.net/~linrunner/+archive/ubuntu/tlp)

Now you can install TLP

    sudo add-apt-repository ppa:linrunner/tlp
    sudo apt-get update
    sudo apt-get install tlp

Start tlp with

    sudo tlp bat
    sudo tlp start


