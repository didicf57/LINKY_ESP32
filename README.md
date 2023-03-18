# LINKY_ESP8266

An ESP8266 is used to monitor Linky TIC frames and record some values to a InfluxDB database.

Due to low power energy available on LINKY interface, the consumption profil have to be managed efficiently.
For this we monitor the received frame for 30 seconds and record some value needed for the database.
Each 30 seconds we wake up the WiFi radio interface and send the datas to the database.

WiFi connection and data writting takes around 1.5 seconds.

The electronic part is in development but some function are already validated.


