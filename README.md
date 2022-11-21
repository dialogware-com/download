# [download.dialogware.com](https://download.dialogware.com/)

Download:
[dialogware_amd64.deb](https://download.dialogware.com/dialogware_amd64.deb)

## Preparation to install Dialogware


```bash
mkdir dialogware
cd dialogware
curl -O https://download.dialogware.com/dialogware_amd64.deb
chmod +rwx dialogware_amd64.deb
```

It was tested on PopOs with Eddy, Eddy is a simple Debian package management GUI tool in Elementary OS that allows installation of Debian packages by dragging and dropping  Debian files onto a GUI window. 
[Install Debian Packages on Elementary OS with Eddy GUI Tool](https://linoxide.com/eddy-install-debian-packages-elementary/)



## Install using gdebi
gdebi is one of the best ways to install deb files on Ubuntu Linux. I prefer this system because it collects all dependencies before installing the main .deb file and because gdebi will try to remove dependency errors while performing an installation.

Before you go installing the deb file, it is best to install gdebi onto your system. Gdebi is available for both the Terminal/Shell and GUI – Graphical User Interface ways. By installing through gdebi, it will be more efficient and faster compared to the Ubuntu software center.
```bash
sudo apt install gdebi-core
```

### Install dialogware using gdebi

```bash
sudo gdebi dialogware_amd64.deb
```

### Apt to install packages (apt-get tool )

There is another way to install deb files on the Ubuntu system, which is an apt-get tool.

```bash
sudo apt install ./dialogware_amd64.deb
```

If your Ubuntu system is old enough, you’ll need to move the deb file into it. The above command will download any dependencies required when running in the Terminal.


or check it:

```bash
sudo dpkg -i dialogware_amd64.deb
```