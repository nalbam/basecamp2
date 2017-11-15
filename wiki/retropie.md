#### wifi
```
sudo vi /etc/wpa_supplicant/wpa_supplicant.conf
```
```
country=US
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
  ssid="nalbam-bs"
  psk="01067684010"
}
```

#### nalbam-rpi
```
git clone https://github.com/nalbam/nalbam-rpi
```
```
./nalbam-rpi/init.sh
./nalbam-rpi/init.sh arcade

npi lcd 8
```

#### rsync
```
rsync -av /Users/nalbam/Downloads/roms/ pi@192.168.150.158:/home/pi/RetroPie/roms/
rsync -av pi@192.168.150.158:/home/pi/RetroPie/roms/ /Users/nalbam/Downloads/roms/
```