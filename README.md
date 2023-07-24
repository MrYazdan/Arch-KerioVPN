# Arch KerioVPN Client
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

## Automatic way :
<pre>
   ~ sudo chmod +x INSTALL
   ~ sudo ./INSTALL
</pre>

### You can use 
<pre>
   ~ kerio -c --> connect
   ~ kerio -d --> disconnect
   ~ kerio -h --> usage :D
</pre>
Connected  ^_^


## Manual way :
<br>
<pre>
   ~ sudo /usr/sbin/kvpnc stop
   ~ sudo /usr/sbin/kvpnc start
   ~ mac=$(cat /var/log/kerio-kvc/debug.log | tr - : | awk '/MAC/ {print $15}' | tail -n 1)
   ~ sudo ip link set kvnet addr $mac
</pre>
Connected  ^_-
<br>

<br>
<br>
<br>

## To Disconnect
<pre>
   ~ sudo /usr/sbin/kvpnc stop
   or
   ~ kerio -d
</pre>
Disconnected !
<br>


