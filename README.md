# KerioVPN Client Arch
Configure kerio vpn client for arch linux distributions such as Manjaro, Endeavouros, BlackArch, ...
![](.temp/kerio-Banner.jpg?raw=true)

<br>

## To Connect :

### 1. Installing KerioVPN Client With AUR
<br>
<pre>
   ~ sudo pacman -S yay     
   ~ yay -S kerio-control-vpnclient
</pre>

### 2. Configure KerioVPN Client
<br>
<pre>
   ~ sudo /usr/sbin/kvpnc configure
</pre>

### 3. Start New Connection To KerioVPN Server
<br>
<pre>
   ~ sudo /usr/sbin/kvpnc stop
   ~ sudo /usr/sbin/kvpnc start
   ~ mac=$(cat /var/log/kerio-kvc/debug.log | grep MAC | tail -1 | tr - : | awk '{print $15}')
   ~ sudo ip link set kvnet addr $mac
</pre>
Connected &#0160  ^_^
<br>
<br>
<br>

## To Disconnect
<pre>
   ~ sudo /usr/sbin/kvpnc stop
</pre>
Disconnected !
<br>


