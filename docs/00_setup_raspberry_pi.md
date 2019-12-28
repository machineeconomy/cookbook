
### Step 1 — Install Raspbian
First, we want to install Raspbian — we recommend to install Raspbian Stretch Lite (Download here). To do that plug the Pi’s SD card in your computer and flash the Raspian Stretch Lite on it. Tip: To do that you can use Etcher.
![Install Raspbian with Etcher](../assets/00_1.png)

### Step 2 — Configure headless WiFi
After the flashing process finished, the SD card has been ejected from your computer. All you need to do is to plug it out and in to let the OS recognize it again. As soon as your boot drive has appeared to open your terminal and go to the SD card directory:

```markdown
$ cd /Volumes/boot
```

### Step 3 — Enable SSH
Now we want to enable SSH, which is disabled by default on the Raspberry Pi. We simply create a file called ssh within the boot drive, which enables SSH on it. To do that run:


```markdown
$ touch ssh
```

Even if the file is empty it will enable ssh as soon as the Pi boots.
Attention: Please change your default passwort!

### Step 4 — Connect to wifi
Lastly, we also want the Pi to connect with wifi as soon as it boots. To do that we store the connection details at the boot drive of the Pi. Execute the following command:

```markdown
$ nano wpa_supplicant.conf
```

Now go ahead and paste the following code in the file. Also, enter your wifi connection details and press ctrl + x to save the changes.
```markdown
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
network={    
    ssid="YOUR_SSID"    
    psk="YOUR_WIFI_PASSWORD"    
    key_mgmt=WPA-PSK
}
```

Tip: If you intend to use the tool in different places you can easily set up multiple wifi configurations right now. By doing so you won’t need to plug out the Pi’s SD card when you change your location. If you want to do that just add the following code:

```markdown
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
     ssid="SCHOOL_NETWORK_NAME"
     psk="SCHOOL_PASSWORD"
     id_str="school"
}
network={
     ssid="HOME_NETWORK_NAME"
     psk="HOME_PASSWORD"
     id_str="home"
}
```

You can add as many networks as you want here by adding more network object.

### Step 5 - Plugin and run!
Close the terminal, plug in the SD card to the PI and turn it on!

### Step 6 — Connect via SSH

Get the IP address of the PI with this command in the terminal

To connect to the Pi via SSH you can execute the following command:

```markdown
$ sshpass -p raspberry ssh -o StrictHostKeyChecking=no pi@raspberrypi.local
```

### Step 7 — Change user password
The default username is “pi” and the password “raspberry”.
Connect to it and change the password directly:

```markdown
$ passwd
```

Input the current password “raspberry” and change it with your own!
![Install Raspbian with Etcher](../assets/00_2.png)


### Step 8 — Install NodeJS
Install NodeJS on your Raspberri Pi.

```markdown
$ sudo apt-get dist-upgrade
$ curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
$ sudo apt-get install -y nodejs
$ node -v 
```


### Step 9 — Install NodeJS
Install git. Git is a free and open source distributed version control system to manage source code.

```markdown
$ sudo apt-get install git
```

### Step 10 — Youre ready!

setup a real project.
