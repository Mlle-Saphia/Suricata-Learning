**LAB-02 - Capture réseau avec Suricata**



**Objectif**

Configurer Suricata pour analyser le trafic réseau réel de la machine.



**Configuration**

Interface utilisée : Wi-Fi



Identifiant Npcap : \\\\Device\\\\NPF\_{C78F8B27-796F-4618-A667-CDF51870C5EB}



Configuration YAML

Le fichier principal utilisé : C:\\Suricata\\suricata.yaml



Les chemins importants :

&#x20;   C:\\Suricata\\log

&#x20;   C:\\Suricata\\rules



Lancement de Suricata

Commande utilisée : .\\suricata.exe -c .\\suricata.yaml -i <interface>



Vérification des logs

Fichiers générés :

fast.log

eve.json

stats.log



Résultat

Suricata capture correctement le trafic réseau et génère des événements.

