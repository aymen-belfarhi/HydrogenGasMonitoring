# HydrogenGasMonitoring
Detecting Hydrogen gas within the air and his concentration, is very ipmportant nowadays. Beceause humans are extremely harmful to hydrogen gas, which produces sparks when mixed with air. As a result, hydrogen gas must be monitored and measured on a regular basis to avoid these problems. It does, however, necessitate the use of a sensor or module. The MQ8 sensor is the first in a series of MQ gas sensors that is specifically intended to detect hydrogen gas.

HydrogenGasMonitoring is a simple function made for [Nuclio](https://nuclio.io/)
, an open source and managed serverless platform that we may install on our own server. [RabitMQ](https://www.rabbitmq.com/) is used as a broker to distribute MQTT messages. It also includes the Mobile Application - [MQTIZER](https://play.google.com/store/apps/details?id=com.sanyamarya.mqtizermqtt_client&hl=en&gl=US)
, which allows you to check Mqtt messages on your mobile device.


# Instructions
First of all, clone this repository, then you need to start a [Docker](https://www.docker.com/)
 to start up a [Docker](https://www.docker.com/)
 instance of [Nuclio](https://nuclio.io/), with the 
command:

`$ sudo docker run -p 8070:8070 -v /var/run/docker.sock:/var/run/docker.sock -v /tmp:/tmp nuclio/dashboard:stable-amd64` 

And to start up a [Docker](https://www.docker.com/) instance of [RabitMQ](https://www.rabbitmq.com/), with the command:

`$ sudo docker run -p 9000:15672 -p 1883:1883 -p 5672:5672 cyrilix/rabbitmq-mqtt`

- [MQTIZER](https://play.google.com/store/apps/details?id=com.sanyamarya.mqtizermqtt_client&hl=en&gl=US)
 is a mobile MQTT client that can connect to any broker which shares the network with your phone, and to any broker on the cloud as well To show Message on Mobile App download Mobile App - [MQTIZER](https://play.google.com/store/apps/details?id=com.sanyamarya.mqtizermqtt_client&hl=en&gl=US)
 than Add the Broker on the app having same Ip as RabitMQ. Now you will be able to see messages on Mobile Application

# Prerequisite
- [Docker](https://www.docker.com/)

- [Nuclio](https://nuclio.io/)

- [RabitMQ](https://www.rabbitmq.com/)

- [Arduino ](https://www.arduino.cc/en/software)

- [MQTIZER](https://play.google.com/store/apps/details?id=com.sanyamarya.mqtizermqtt_client&hl=en&gl=US)

# Libraries used
-  ESP8266WiFi

The ESP8266WiFi library provides a wide collection of C++ methods (functions) and properties to configure and operate an ESP8266 module in station and / or soft access point mode.

-  PubSub Client

A client library for MQTT messaging. MQTT is a lightweight messaging protocol ideal for small devices. This library allows you to send and receive MQTT messages.
