# Creating a Hacking Lab
## Assignment 6

To creating this lab we will be using kvm

To install the same follow the guide at :
https://github.com/abhinavmk00/Writeups/blob/main/Day%206/report_6.md

Open virtual machine manger
![](./pics/1.png)
Go to edit and enable xml editing
![](./pics/2.png)
Select local install media
![](./pics/3.png)
Click browse
![](./pics/4.png)
Click browse local
![](./pics/5.png)
Select the windows .iso file
![](./pics/6.png)
Click Forward
![](./pics/7.png)
![](./pics/8.png)
Select the ram and the cpu 
![](./pics/9.png)
Now select the amount of storage
![](./pics/10.png)
Check the Coustomize configuration
![](./pics/11.png)
Select overview and select xml and paste the following 
```
<hyperv mode="custom">
  <relaxed state="on"/>
  <vapic state="on"/>
  <spinlocks state="on" retries="8191"/>
  <vpindex state="on"/>
  <runtime state="on"/>
  <synic state="on"/>
  <stimer state="on">
    <direct state="on"/>
  </stimer>
  <reset state="on"/>
  <vendor_id state="on" value="KVM Hv"/>
  <frequencies state="on"/>
  <reenlightenment state="on"/>
  <tlbflush state="on"/>
  <ipi state="on"/>
  <evmcs state="on"/>
</hyperv>
```
![](./pics/12.png)
![](./pics/13.png)
![](./pics/14.png)
change the disk bus to virtio
![](./pics/15.png)
![](./pics/16.png)
Download the virtio drivers
```
$ wget https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/archive-virtio/virtio-win-0.1.240-1/virtio-win-0.1.240.iso
```
![](./pics/17.png)
Add the virtio iso to the vm
![](./pics/18.png)
![](./pics/19.png)
![](./pics/20.png)
Change the nic to virtio
![](./pics/21.png)
Remove tablet support
![](./pics/22.png)
Change the version to 2.0
![](./pics/23.png)
Click begin installation
![](./pics/24.png)
Select the windows iso in the bios
![](./pics/25.png)
Select the language and keyboard
![](./pics/26.png)
Finish the windows install
![](./pics/27.png)
To be continued ....