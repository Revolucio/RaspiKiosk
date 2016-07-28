## RaspiKiosk

A simply way to have a Raspberry Pi in kiosk mode.


## Motivation

I needed to see a web page with monitoring data, so I simply need a monitor displaying a web page.

## Parts

A [Rasperry Pi](https://www.raspberrypi.org/ "Raspberry Pi").


## Setup

Once installed the OS be sure you have installed:
	
- Clone the repo
- **chromium**: see [http://raspberrypi.stackexchange.com/questions/44384/how-to-get-chromium-on-raspberry-3](http://raspberrypi.stackexchange.com/questions/44384/how-to-get-chromium-on-raspberry-3)
- **matchbox**: `apt-get install -y matchbox-window-manager`

## Customization

Edit *startx_kiosk.sh* and change the URL on the line: 

	matchbox-window-manager & chromium --kiosk URL

for instance:

	matchbox-window-manager & chromium --kiosk http://github.com

## Run
	
Be sure *startx_kiosk.sh* has execution permissions doing:

	chmod u+x startx_kiosk.sh

and execute it 

	./startx_kiosk.sh &