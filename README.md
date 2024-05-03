# Async communication Example with Reference Workshop Net

## Description
This repository contains a model, consisting of reference nets build with the Reference Net Workshop tool (http://www.renew.de/).

The model demonstrates how to implement asynchronous bi-directional communication using the MQTT protocol between a net model and physical devices.
## Description of the case to be modeled

A scenario consisting of floodgates and a panic button has been modeled. The gates are initially open and then go into a closed state, remaining in this loop until the panic button is pressed. At this point, the gates stop moving and stay motionless until their movement in the previous or opposite direction is resumed.
## Model description
The model consists of the following networks:

* **Controller -** Reference net that displays the state of the *Cyber-Physical Systems* (CPS)
* **Gate -** Reference net that represents the gates' digital counterpart.
* **Button -** Reference net that represents the digital counterpart of a CPS for the panic button.
* **Communiator -** Reference net that instantiates the MQTT client class and enables communication between the networks of the logical part of the CPS and its counterpart.
* **mqtt_message_receiver -** Reference net used as an observer in the Java class to receive messages and pass them on to the other networks synchronously between transitions.


