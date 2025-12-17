1-	Install vmware:
Windows: // peronally did not do this one but got the link form christopher
https://www.techspot.com/downloads/189-vmware-workstation-for-windows.html
mac: 
if your device is old use this
https://vmware-fusion.en.uptodown.com/mac/download/3438691

if not use this
https://vmware-fusion.en.uptodown.com/mac/download/

notes:
*download button in green bottom left for the mac websites 
*you will need some sort of license to install it.I got 30 days trial for now. Then contact boardcom support later or something

2-	Ubuntu 
https://releases.ubuntu.com/jammy/

3-	Then its pretty straightforward to drag the ubuntu to the vmware application and start ubuntu
4-	Ros2 humble installation:
Open your terminal in ubuntu:
Write these commands by order just copy paste


sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8
/////////////
sudo apt install software-properties-common
sudo add-apt-repository universe
////////
sudo apt update && sudo apt install curl -y
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
//////////
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
//////////
sudo apt update
////////
sudo apt upgrade
///////
sudo apt install ros-humble-desktop

5-last step which is to (set a permenant ros environment)
In your terminal write
 ~/.bashrc 
And then a file will open go to the last line numbered 119 and write:
Source /opt/ros/humble/setup.bash

And SAVE
Reference:
https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html
<img width="451" height="684" alt="image" src="https://github.com/user-attachments/assets/9434f4b7-1688-4fea-b335-1c3df0838181" />
