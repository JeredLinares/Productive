# Productive
Productivity increase using RPi

#Setup

## Setup Startup



## Setup Hourly
Cron job


# Audio Tone
440Hz 5 sec


# NOTES
## Wifi Conection
At boot folder
	Add file >> wpa_supplicant.conf
```
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=<Insert 2 letter ISO 3166-1 country code here>

network={
        scan_ssid=1
        ssid="<Name of your wireless LAN>"
        psk="<Password for your wireless LAN>"
        proto=RSN
        key_mgmt=WPA-PSK
        pairwise=CCMP
        auth_alg=OPEN
}
```

## Audio
https://www.raspberrypi.org/documentation/usage/audio/README.md
https://www.raspberrypi.org/documentation/raspbian/applications/omxplayer.md

## 

