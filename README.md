# LINKY_ESP8266

Un ESP8266 est utilisé pour lire les trames TIC venant du compteur Linky et de les enregistrer periodiquement dans une base InfluxDB.

Du fait de la faible energie fournie par le compteur, un stratégie de lecture vs depot est necessaire.
Alors que les trames evoluent toutes les secondes, Le depot sur InfluxDb se fait en WiFi toutes les 30 secondes. 
Il y a donc un prétraitement fait en local par l'ESP8266.

La durée de connexion est d'environ 2 secondes et la consommation de 70mA.
Pendant le prétraitement , la consommation est de 10/20mA.
La configuration des accés WiFi se fait dans le code source.

Le code ne remonte que l'index général, mais peut tout a fait remonter les index HC/HP plus jours rouge/blanc/bleu (a venir)

Le schema et le PCB est disponible :
-Redressement (diode), 
-SuperCapa + Zener (reserve energie)
-Alimentation (LDO) piloté par superviseur de tension
-Mise en forme des trames Linky (opto et démodulation)
-Support pour ESP
-Pads pour fils de connexion au Linky
-Interface entre les deux PCB

Toutes suggestions en vue d'amélioration sont bienvenues.
