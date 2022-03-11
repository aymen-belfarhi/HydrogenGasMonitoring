# HydrogenGasMonitoring
Detecting Hydrogen gas within the air and his concentration, is very ipmportant nowadays. Beceause humans are extremely harmful to hydrogen gas, which produces sparks when mixed with air. As a result, hydrogen gas must be monitored and measured on a regular basis to avoid these problems. It does, however, necessitate the use of a sensor or module. The [MQ8 SENSOR ](https://components101.com/sensors/mq8-hydrogen-gas-sensor-pinout-features-datasheet-working-alternative-application) is the first in a series of MQ gas sensors that is specifically intended to detect hydrogen gas.

HydrogenGasMonitoring is a simple function made for [Nuclio](https://nuclio.io/)
, an open source and managed serverless platform that we may install on our own server. [RabitMQ](https://www.rabbitmq.com/) is used as a broker to distribute MQTT messages. It also includes the Mobile Application - [MQTIZER](https://play.google.com/store/apps/details?id=com.sanyamarya.mqtizermqtt_client&hl=en&gl=US)
, which allows you to check Mqtt messages on your mobile device.


# Requirements
- [MQ8 SENSOR ](https://components101.com/sensors/mq8-hydrogen-gas-sensor-pinout-features-datasheet-working-alternative-application)

- [ESP8266 ](https://fr.wikipedia.org/wiki/ESP8266)

- [Arduino IDE ](https://www.arduino.cc/en/software)

- [Nuclio](https://nuclio.io/)

- [RabitMQ](https://www.rabbitmq.com/)

- [Docker](https://www.docker.com/)

- [MQTIZER](https://play.google.com/store/apps/details?id=com.sanyamarya.mqtizermqtt_client&hl=en&gl=US)

# Instructions
The first step is to start [Docker](https://www.docker.com/) and initiate the [Nuclio](https://nuclio.io/) instance by using the following command :

`$ sudo docker run -p 8070:8070 -v /var/run/docker.sock:/var/run/docker.sock -v /tmp:/tmp nuclio/dashboard:stable-amd64` 

use the following command to initiate the [Docker](https://www.docker.com/) instance of [RabitMQ](https://www.rabbitmq.com/)

`$ sudo docker run -p 9000:15672 -p 1883:1883 -p 5672:5672 cyrilix/rabbitmq-mqtt`

- [MQTIZER](https://play.google.com/store/apps/details?id=com.sanyamarya.mqtizermqtt_client&hl=en&gl=US)
 is a mobile MQTT client that can connect to any broker which shares the network with your phone, and to any broker on the cloud as well To show Message on Mobile App download Mobile App - [MQTIZER](https://play.google.com/store/apps/details?id=com.sanyamarya.mqtizermqtt_client&hl=en&gl=US)
 than Add the Broker on the app having same Ip as RabitMQ. Now you will be able to see messages on Mobile Application


# Libraries used in this work
-  First library is PubSubClient:

A client library for MQTT messaging. This library allows you to send and receive MQTT messages. It supports the latest MQTT 3.1.1 protocol and can be configured to use the older MQTT 3.1 if needed. It supports all Arduino Ethernet Client compatible hardware, including the Intel Galileo/Edison, ESP8266 and TI CC3000.

-  Second one is ESP8266WiFi:

ESP8266 is all about Wi-Fi. If you are eager to connect your new ESP8266 module to Wi-Fi network to start sending and receiving data, this is a good place to start. If you are looking for more in depth details of how to program specific Wi-Fi networking functionality, you are also in the right place.

