# SmallProjects
A few short descriptions of things I implemented at home using what I learned in the Microsoft Academy.

# Setting up Hyper-V
Setting up my Windows 10 Computer for Hyper-V and Hypervisor, I discovered I needed to upgrade my Windows Home version. Luckily ERAU provided me with access to a free verison on Windows 10's Education Edition. Having upgraded to Windows 10 Education, I attempted to create a VM only to receive an error that hypervisor was not enabled. I opened the Windows Features to ensure I had all the Hyper-V related options enabled, and they were. With a little research, I discovered that my CPU had virtualization disabled. To enable virtualization, I had to access the BIOs startup advanced setting and enabled it on my CPU.

# Creating a Windows Server 2016 VM
Having set up my computer for virtualization the first thing I wanted to do was set up a VM with Windows Server 2016. So I created a Generation 2 VM with 4GB of RAM, 32gb of storage and Windows Server 2016 Standard Edition. I took screenshots during my process and will provide step by step instructions on how you can make your own.

# Setting up Docker
While trying to install and enable Docker through PowerShell on my VM I was running getting an error stating it was “Unable to download from URI” during the Install-Module request. After verifying internet connection functionality using ping in PowerShell, I began to research the problem. I discovered that in Windows Server 2016, running PowerShell 5.1 will use deprecated security protocols. Through PowerShell, I confirmed that my security protocols in the system where SSL3 and TLS1. So, to fix my download error I just needed to enable TLS1.2, allowing my Install-Module command to finally work as intended and set up Docker on my Windows Server 2016 VM.
