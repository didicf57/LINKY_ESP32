# LINKY_ESP8266

Un ESP8266 est utilisé pour lire les trames TIC venant du compteur Linky et de les enregistrer periodiquement dans une base InfluxDB.

Du fait de la faible energie fournie par le compteur, un stratégie de lecture vs depot est necessaire.
Alors que les trames evoluent toutes les secondes, Le depot sur InfluxDb se fait en WiFi toutes les 30 secondes. 
Il y a donc un prétraitement fait en local par l'ESP8266.

La durée de connexion est d'environ 2 secondes et la consommation de 70mA.
Pendant le prétraitement , la consommation est de 10/20mA.

La configuration des accés WiFi se fait dans le code source.

La carte electronique est en developpement mais des fonctions sont déjà validées
-Redressement, 
-SuperCapa, 
-Alimentation (LDO)
-Mise en forme des trames Linky (opto et démodulation)

a suivre

