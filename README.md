# Library-Raspberry-Pi4
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python3
sudo apt-get install build-essential python3-dev
sudo python3 setup.py install

#Grove seeed
curl -sL https://github.com/Seeed-Studio/grove.py/raw/master/install.sh | sudo bash -s -
sudo pip3 install seeed-python-dht

#DHT Adafruit
cd /
sudo apt-get update
sudo apt-get install build-essential python3-dev
sudo git clone https://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT
sudo python3 setup.py install

#MQTT
sudo pip3 install paho-mqtt

sudo pip3 install fastapi[all]
sudo pip3 install uvicorn
sudo pip3 install pymongo

#Supervisor
sudo apt-get install supervisor
