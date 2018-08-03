# Mosquitto MQTT Server 
When Publisher sends a message to a topic, the Subscriber subscribing to the topic receives the message through the MQTT Broker.

## Installing mosquitto on Windows

1. Download the windows installation file.

	  ``mosquitto-1.4.15a-install-win32.exe``  from <https://mosquitto.org/download/>
2. Click the link and download.

	![test](C:\Users\Pearl2\Downloads\cap.jpg)

	* ``Win32 OpenSSL v1.0.2o Light``
	
	* ``pthreadVC2.dll``
3. Open **" C:\OpenSSL-Win32 "**.
   
    Copy **all .dll files** and paste on 
**" C:\Program Files (x86)\mosquitto "**.

4. Copy the **pthreadVC2.dll** file that was downloaded earlier on **" C:\Program Files (x86)\mosquitto "**.


## Run mosquitto subscriber, publisher
* Open two Command Prompt programs.

* >cd /

	>cd "Program Files (x86)\mosquitto" 

* First cmd
    mosquitto_sub -h "host" -t "topic name" -p "port number"
    ex) mosquitto_sub -h 192.168.0.15 -t /home/set -p 1883

* Second cmd    
    mosquitto_pub -h "host" -t "topic name" -m "message" -V mqttv311
    ex) mosquitto_pub -h 192.168.0.15 -t /home/set -m "ON" -V mqttv311
 
* Check communication.
