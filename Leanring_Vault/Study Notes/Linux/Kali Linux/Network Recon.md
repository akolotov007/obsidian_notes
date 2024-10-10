`nmcli dev wifi`
shows devices that have a wifi signal 
 better than `iwlist` 
pg 195 | linux basics for hackers

___
check processes to kill before placing into monitor mode
`airmon-ng check kill`

wireless card into monitor mode
`airmon-ng start|stop|restart interface`

*your wireless card name will change : wlan0 => wlan0mon*

finding data on wireless traffic with airodump-ng
`airodump-ng`
![[Pasted image 20241002194146.png]]
now you can filter by BSSID of the network and focus on it

![[Pasted image 20241002194510.png]]


after this, we can open up another terminal that will focus on de-authing a device on the network that we choose


