# Get-VNCViewer-to-access-Ubuntu14.04

In Ubuntu 14.04, even after enabling Remote Desktop, encryption is on by default which forces refusal of connection by VNC Viewer on other machines that try to connect to the Ubuntu machine, hence the encryption needs to be set to off.

DO the following for it:

install dconf-tools:

sudo apt-get install dconf-tools

dconf-editor

Go to:
org -> gnome -> desktop -> remote-access & uncheck require-encryption

gsettings set org.gnome.Vino require-encryption false

Now try putting just the IP and connect!
