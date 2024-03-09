## <a name="introduction">💻 AWS IoT Configuration Guide for ESP8266</a>

<img src="https://github.com/rch-goldsnaker/aws-esp8266/blob/main//banner.png" alt="Project Banner">

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. ⚙️ [Tech Stack](#tech-stack)
3. 🔋 [Features](#features)
4. 💻 [Youtube tutorial](#youtube)
5. 🤸 [Quick Start](#quick-start)
   
## <a name="introduction">🤖 Introduction</a>

This repository has code for an ESP8266-based MQTT client. It connects to AWS IoT Core service. The device sends random temperature and humidity data to an MQTT topic regularly. It also listens to another topic for commands.

## <a name="tech-stack">⚙️ Tech Stack</a>

💎 ESP8266 

💎 Arduino Framework

💎 AWS IoT Core

💎 MQTT Protocol

💎 ArduinoJson Library

## <a name="features">🔋 Features</a>

👉 WiFi Connection: It connects to the internet using WiFi, enabling communication with other devices and services.

👉 Secure Connection to AWS IoT: It securely connects to AWS IoT, a cloud service, to exchange data without unauthorized access.

👉 Sending Random Data: It sends randomly generated temperature and humidity data in a format that's easy for other devices to understand.

## <a name="youtube">💻 Youtube tutorial</a>

See tutorial video [here](https://youtu.be/xZoeJ-osS3g)

## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up the project locally on your machine.

**Prerequisites**

Make sure you have the following installed on your machine:

- Git (https://git-scm.com/)
- Arduino IDE (https://www.arduino.cc/en/software)

Install Board:
- esp8266 by ESP8266 Community (https://github.com/esp8266/Arduino)

Install library:
- PubSubClient by Nick O’Leary (https://pubsubclient.knolleary.net/)
- ArduinoJson by Benoit Blanchon (https://arduinojson.org/?utm_source=meta&utm_medium=library.properties)

**Cloning the Repository**

```bash
git clone https://github.com/rch-goldsnaker/aws-esp8266
cd aws-esp8266
```

**Set Up certificates from AWS**

```env
//Amazon trust services endpoint
static const char cacert[] PROGMEM = R"EOF(
-----BEGIN CERTIFICATE-----
-----END CERTIFICATE-----
)EOF";

//Device certificate
static const char client_cert[] PROGMEM = R"KEY(
-----BEGIN CERTIFICATE-----
-----END CERTIFICATE-----
)KEY";


//Private key file
static const char privkey[] PROGMEM = R"KEY(
-----BEGIN RSA PRIVATE KEY-----
-----END RSA PRIVATE KEY-----
)KEY";
```

**Set Up your Device name and MQTT broker host**

```bash
// Device name from AWS
const char THINGNAME[] = "********";

// MQTT broker host address from AWS
const char MQTT_HOST[] = "********";
```

**Set Up your Wifi Credential**

```bash
// WiFi credentials
const char WIFI_SSID[] = "********";
const char WIFI_PASSWORD[] = "********";
```

Copy the code to Arduino IDE and Upload
