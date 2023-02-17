---
hide:
    - toc
---

# February 9th 2023 : Design and Prototyping


**Reflection**

"We can measure almost anything if we have something that reacts to the change. We can then measure that reaction"


^^Assignment:try to use a sensor and and actuator to communicate^^


(done with the help of brother and translated back as best possible) 


To make a sensor and an actuator communicate using an ESP32 Feather board, you can use a communication protocol such as MQTT. Here are the steps you can follow:
1. Set up the ESP32 Feather board and connect the sensor and the actuator to the board's GPIO pins.

2. Install the necessary software tools, such as the Arduino IDE and the ESP32 board support package.

3. Install the MQTT library in the Arduino IDE, such as the "PubSubClient" library.

4. Set up an MQTT broker, which is a message broker that enables communication between devices. You can use a cloud-based broker service such as AWS IoT or a local broker such as Mosquitto.

5. In the sketch, include the necessary libraries for the ESP32, the sensor, and the actuator, as well as the "PubSubClient" library.

6. Connect the ESP32 to the MQTT broker by specifying the broker's IP address, port, and client ID. You will also need to set up a username and password if the broker requires authentication.

7. Publish the sensor data to an MQTT topic by using the "publish" function. The topic is a string that identifies the data being published, such as "sensor/temperature".

8. Subscribe to the MQTT topic that controls the actuator by using the "subscribe" function. The topic is a string that identifies the control message, such as "actuator/control".

9. In the callback function for the subscribed topic, read the control message and perform the appropriate action on the actuator, such as turning it on or off.

10. Upload the sketch to the ESP32 Feather board and test the communication by sending control messages to the actuator from a separate device or application.


The following code communicates between a DHT11 temperature and humidity sensor and an LED actuator using MQTT:

  }#include <WiFi.h>
  #include <PubSubClient.h>
  #include <Adafruit_Sensor.h>
  #include <DHT.h>
  
  // Wi-Fi settings
  const char* ssid = "your_SSID";
  const char* password = "your_PASSWORD";
  
  // MQTT broker settings
  const char* mqtt_server = "your_MQTT_broker_IP_address";
  const char* mqtt_username = "your_MQTT_username";
  const char* mqtt_password = "your_MQTT_password";
  const char* mqtt_client_id = "esp32_client";
  
  // MQTT topics
  const char* sensor_topic = "sensor/temperature_humidity";
  const char* actuator_topic = "actuator/led_control";
  
  // DHT11 settings
  #define DHTPIN 4
  #define DHTTYPE DHT11
  DHT dht(DHTPIN, DHTTYPE);
  
  // LED actuator settings
  const int led_pin = 5;
  
  // Wi-Fi client and MQTT client
  WiFiClient espClient;
  PubSubClient mqtt_client(espClient);
  
  void setup() {
  // set the LED pin as an output
  pinMode(led_pin, OUTPUT);
  
  // start the serial communication
  Serial.begin(9600);

  // connect to Wi-Fi
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to Wi-Fi...");
  }
  Serial.println("Connected to Wi-Fi");

  // connect to MQTT broker
  mqtt_client.setServer(mqtt_server, 1883);
  mqtt_client.setCallback(callback);
  while (!mqtt_client.connected()) {
    Serial.println("Connecting to MQTT broker...");
    if (mqtt_client.connect(mqtt_client_id, mqtt_username, mqtt_password)) {
      Serial.println("Connected to MQTT broker");
      mqtt_client.subscribe(actuator_topic);
    } else {
      Serial.print("Failed with




