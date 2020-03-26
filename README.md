# EasyRO (Inactive)
## I decided to stop a few of my projects. The reason is that there's more time for future projects.
## Make root filesystem read-only!

### About
EasyRO is a script providing read-only mode and read-write mode. It's aimed on 'trying to make it simpler for everyone to make a read-only system'. This can be for many different purposes. such as: self-build router, vpn server etc.

### Instructions
If you don't want to read instructions about how it works, then only run the following command:

  *curl https://tomaaien.nl/easyro/install | bash*
  

#### Prerequisite
You need: curl, wget, root access and bash.

#### Testing and stable
I've made two version: the testing branch and stable branch. The testing branch is heavily tested when new updates are implemented. At the moment those two are the same.

If you want to install the *stable*  branch:

  *curl https://tomaaien.nl/easyro/install | bash*
  
If you want to install the *testing*  branch:
  
  *curl https://tomaaien.nl/easyro/testing/install | bash*
  
### Extra information
There are 2 commands when installed: easyro-ro and easyro-rw. The first one makes you root filesystem read-only. The second one makes your filesystem read-write.

The last one: when booting your device, it takes 60 seconds to make the fs (filesystem) read-only. That happens automatically. The reason is that some services refuse to start if the filesystem is read-only at boot. That's why I made this script.

### Uninstall

If you want to remove this script you can do 2 things: or you remove it completely or you remove only the script and replace the rc.local file with the original one.

If you want to remove it completely (as root):
  
  *rm /etc/systemd/system/rc-local.service /etc/rc.local /usr/local/bin/easy-r**
  
And then reboot.


If you want to replace rc.local with the original one and remove the script (as root):

  *rm /etc/rc.local /usr/local/bin/easy-r**
  
Then you create a new rc.local with the rc.local on this GitHub page (master branch => rc.local-restore).
If copy it, paste it in /etc/rc.local with your favorite text/programming editor.

Then reboot.

## Cheers!
