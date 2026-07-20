**LAB-03 - Première règle Suricata personnalisée**



**Objectif**



Créer une première règle personnelle permettant de détecter un événement réseau.



**Création de la règle**



Fichier créé : C:\\Suricata\\rules\\local.rules



Contenu : alert icmp any any -> any any (msg:"\[LAB] Ping détecté"; sid:1000001; rev:1;)



**Explication**



\-   alert : génère une alerte

\-   icmp : surveille le protocole ICMP utilisé par le ping

\-   any any : toutes les adresses et tous les ports

\-   msg : message affiché dans les logs

\-   sid : identifiant unique de la règle

\-   rev : version de la règle



**Test**



Envoyer un ping : ping 8.8.8.8



Puis vérifier : C:\\Suricata\\log\\fast.log



**Résultat du test**



La règle a été chargée correctement.



Commande de validation : .\\suricata.exe -T -c .\\suricata.yaml



Résultat :



Configuration provided was successfully loaded.



Test réalisé : ping 8.8.8.8



Alerte obtenue dans fast.log :



\[1:1000001:1] \[LAB] Ping détecté



La première règle personnalisée Suricata fonctionne.

