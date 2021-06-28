# Productive
Productivity increase using RPi

# Jobs

## Setup Hourly between 6am and 7pm Monday - Friday
Cron job
At minute 0 past every hour from 6 through 19 on every day-of-week from Monday through Friday.
0 6-19 * * 1-5				


# Audio Tone
440Hz 5 sec
	/sharedSpace/audio


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
Play sound
	omxplayer -o local example.mp3		// "local" play through headphone jack



https://www.raspberrypi.org/documentation/usage/audio/README.md
https://www.raspberrypi.org/documentation/raspbian/applications/omxplayer.md
NOTE: omxplayer does not use raspi-config or amixer settings


## Scheduling
Cron
	crontab: cron table (per user) 
	crontab -l : list scheduled tasks
	@reboot : add for on startup
	& : add at the end for background process
Syntax
	minute 	hour	dayOfMonth	month	dayOfWeek	

https://www.raspberrypi.org/documentation/linux/usage/cron.md


## VIM notes
dt 'character'			// delete to character
{ or } 					// jump one paragraph


## Permissions
chmod
	777 all 

## User groups
list
	

## Errors
>> failed to open vchiq
	omxplayer needs to be in the audio and video groups
	add to group "video"
		usermod -aG video testuser






