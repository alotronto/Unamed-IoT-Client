#Unamed-IoT-Client

**Unamed-IoT-Client** is the client to connect Arduino YUN/Linino One or Raspberry Pi to [**Unamed-IoT-Cloud**](https://github.com/alotronto/Unamed-IoT-Client.git), to works correctly there is some specification for the devices:

* Arduino YUN/Linino ONE:

	* LininoIO O.S.;

	* Nodejs;

* Raspebery Pi:
	
	* Nodejs;

##Arudino YUN/Linino One Installation Dependencies
To install the last version of LininoIO O.S. on Arduino YUN/Linino ONE it is usefull to consult the Linino wiki where there is a [guide](http://wiki.linino.org/doku.php?id=wiki:upgradetolininoio) to upgrade the board to LininoIO O.S. . 

After the LininoIO O.S. is installed on the board you need to install Nodejs on the board, you can use the [guide](http://wiki.linino.org/doku.php?id=wiki:nodejscript) to install Nodejs using a simple bash script on the official Linino wiki page. 

##Raspberry Pi Installation Dependencies
You can use a Rapseberry Pi with any kind of O.S. we have tested the **Unamed-IoT-Client** on Rasperry Pi with *Raspbian*. To install Nodejs on Raspberry Pi with *Raspbian* just use the package manager of the O.S. using the follow command:

```
suo apt-get install nodejs
```

##Install node-lighthing-rod##

To install the client **Unamed-IoT-Client** you need to copy on the board all the source code in the github repository, after you have copied the source code, you can use the python script *install.py*, at the root directory of the source code, to install the client and the boot service on the board, to do this you can use the follow command:

```
python install.py yun|rasp
```

*yun* paramiter for Arduino YUN/Linino One devices or *rasp* paramiter for Raspberry Pi devices.

##Configuration
After you have installed the client **node-lighthing-rod** you need to edit the configuration file:
```
/opt/node-lighthing-rod/setting.json
```
You need to change the value of the IP and the PORT of the WAMP Router, Reverse Websocket Tunnel Server and other configuration paramiters 