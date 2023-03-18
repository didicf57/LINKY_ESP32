# LINKY_ESP32


ESP32 is used to monitor Linky TIC frame and record it to a InfluxDB database.

Due to low power available on LINKY interface, the consumption profil have to be managed efficiently.
For this we monitor the received frame for 30 seconds and record some value needed for the database.
Each 30 seconds we wake up the WiFi radio interface and send the datas to the database.

WiFi connection and data writting takes around 1.5 seconds.

The electronic part is in devellopment but some function are already validated.


