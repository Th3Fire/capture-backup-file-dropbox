# capture-backup-file-dropbox
Capture photo and backup to Dropbox (API) from Raspberry Pibackup by press switch from ET-TEST 10P/INP

## Firt step
* You need a DropBox account. Hop on over to https://www.dropbox.com/getspace --it's free.

## Device
* USB Web Cam
* Raspberry Pi
* ET-TEST 10P/INP

## Install package
```bash
sudo apt-get install python-opencv
sudo apt-get install git
```

## Download and set up DropBox Uploader (clone this repository)
```bash
git clone https://github.com/wuttinunt/capture-backup-file-dropbox.git

cd capture-backup-file-dropbox

git clone https://github.com/andreafabrizi/Dropbox-Uploader.git

cd Dropbox-Uploader
```

Run the script with ```./dropbox_uploader.sh``` (if it fails, try chmod +x dropbox_uploader.sh)
You should see this...
![setAPI](setAPI.jpg?raw=true "setAPI")

Then, You need to visit this link https://www.dropbox.com/developers/apps (must logged in) and follow this

1. Click ```Create app``` button
2. Choose an API > ```Dropbox API
3. Choose the type of access > App folder (up to you in my case I want access for some folder)
4. Set up name your app and then click Create app button
5. Now look at App key and click show App secret you need use it for set up for next step
6. At Shell input your App key ```Enter``` 
7. Once you've entered your keys and answered the question "app" or "full" your Pi will request an authorisation token and you will be given a web URL you need to visit to activate it and clink ```Allow``` If it works, you should see this in your browser… Success!

## Prepair before run program
1.Connect jumper wire look at table

| GPIO raspberry pi (pin)| ET-TEST 10P/INP (pin) |
|:----------------------:|:---------------------:|
|           16           |           1           |
|           2 (5V)       |           10 (5V)     |
|           6 (GND)      |           9 (GND)    |


![GPIO](GPIO.png?raw=true "GPIO")

credit image http://grimbodroid.blogspot.com/2012/08/following-directions-on-these-pages-1.html

2.Connect USB Web Cam to Raspberry Pi

