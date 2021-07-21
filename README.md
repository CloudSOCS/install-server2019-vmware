![CloudSOC logo](https://1.bp.blogspot.com/-YaqntajfnjI/YPcbjtDTuRI/AAAAAAAAAH4/PPe7LLbuo6sipM1cWVIT5FdBC7wzPG54gCLcBGAsYHQ/s150/cloudsoc.png)


Install Windows Server 2019 on VMWare Fusion
------
We are going to need access to some kind of virtualization software. For this example, I’ll be using VMware Fusion Pro, a premium option. However, if you do not have this software it isn't necessary and the free version, VMware Fusion Player will suffice.
We will also need to download a copy of Window server 2019 from the Microsoft Evaluation Centre

You can also scroll down to the end of this tutorial and watch the video on how to install windows server 2019 on vmware fusion.

![2021-07-20_23-30-11.png](/pics/2021-07-20_23-30-11.png)

In the virtual machine library select new:

![1.png](/pics/1.png)

A new window will come up that looks like this:

![2.png](/pics/2.png)

Click continue and then click on Use another disc or disc image..

![3.png](/pics/3.png)

A new window will open, now select the iso image you downloaded from the  [Microsoft Evaluation Centre](https://www.microsoft.com/en-gb/evalcenter/). I downloaded the evaluation iso to my Desktop.
Double click on the iso and it will open a new window, now click continue.

![6.png](/pics/6.png)

Deselect Easy install and click continue, and then click continue again.

![7.png](/pics/7.png)

Click on Customise Settings.

A new window opens and now you can name the serve whatever you would like, I will just leave it as Windows Server 2019. You can also select another drive, as I have done on a backUP drive.

![8.png](/pics/8.png)

Now click save.
Two different windows will come up, one is for Settings and the other is the player that we will select when we are finished configuring our settings.

![9.png](/pics/9.png)

Before we can configure our settings, we need to configure a custom network connection with a Subnet IP. On the top task bar click on  VMware Fusion and then on Preferences

![10.png](/pics/10.png)

In the prefence window select network and then select the + and a vmnet will be in the Custom window, in my case it is vmnet4. Now  in the Subnet IP: window enter 192.168.95.0, also select the Allow virtual machines on this network to connect to external networks (using NAT). We are not going to use IPV6.

![11.pmg](/pics/11.png)

Now click apply and then enter your login password that you use to login to your Mac.

![12.png](/pics/12.png)

Now close the network preference window.
Now lets go to our settings window and select Processors & Memory

![13.png](/pics/13.png)

Select 4 processor cores and 4096 MB of memory.

![14.png](/pics/14.png)

Now click on Show all and we will adjust the Display as picture here.

![15.png](/pics/15.png)

Click show all again and then select Network Adaptor and select the vmnet we created earlier, mine is vmnet4, and then select Advanced options and click generate a new MAC Address.

![16.png](/pics/16.png)

Click on Show all again. Then click on Hard Disk. For Bus type I selected NVMe and selected 75 GB for the Hard Disk size, should plenty for what we are doing.

![17.png](/pics/17.png)

Now close the setting window

Now start the player, the loader from CD comes up fast so be ready to select enter.
A window for windows setup will come up, click next.

![18.png](/pics/18.png)

Install now.

![19.png](/pics/19.png)

Select the operating system, we will be using Windows Server 2019 Datacenter Eval with (desktop experince)

![20.png](/pics/20.png)

Next: Then select I accept the license terms

![21.png](/pics/21.png)

Next. Select custom install.

![22.png](/pics/22.png)

The next window will ask where do you want to install windows , we will use the default. Click next.

![23.png](/pics/23.png)

It will take a few minutes to install, then a window will come up and as for an administrator password, I used pass@word1, I would never use this password on a production server, however for what we are doing its fine.
The next window will ask to Ctrl+Alt+Delete to unlock, go to your top task bar select Virtual Machine and then select Send Control Alt Delete

![25.png](/pics/25.png)

Enter your password ( pass@word1)
We have now installed server 2019.

![png.27](/pics/27.png)

The first thing we will do is install VMware tools

![28.png](/pics/28.png)

![29.png](/pics/29.png)

![30.png](/pics/30.png)

Then click next, and install. Finish and then restart. Now we can adjust our display screen size after the server reboots.

That's it we have now installed Windows Server 2019 using VMware Fusion, My next post will be on how to configure our new server with Active Directory, DNS and DHCP to Create a Domain Controller.
WATCH: How to Install Windows Server 2019 with VMware Fusion

[![Install Windows Server 2019 on VMware Fusion.](https://res.cloudinary.com/marcomontalbano/image/upload/v1626830060/video_to_markdown/images/youtube--KUHe0iTnqGI-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/KUHe0iTnqGI "Install Windows Server 2019 on VMware Fusion.")
