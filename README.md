# Emoncms Wifi Module 

Wifi configuration module for emoncms. Installed on emonPi pre-built SD card image 

![wifi-config](http://openenergymonitor.org/emon/sites/default/files/wifi-config.png)

# Install 
```
  cd /var/www/emoncms/Module
  git clone https://github.com/emoncms/wifi
  ```
  
Give web user permission to execute system wlan commans:

```
  www-data ALL=(ALL) NOPASSWD:/sbin/ifdown wlan0,/sbin/ifup wlan0,/bin/cat /etc/wpa_supplicant/wpa_supplicant.conf,/bin/cp /tmp/wifidata /etc/wpa_supplicant/wpa_supplicant.conf,/sbin/wpa_cli scan_results,/sbin/wpa_cli scan,/bin/cp /tmp/hostapddata /etc/hostapd/hostapd.conf,/etc/init.d/hostapd start,/etc/init.d/hostapd stop,/etc/init.d/dnsmasq start,/etc/init.d/dnsmasq stop,/bin/cp /tmp/dhcpddata /etc/dnsmasq.conf
```
