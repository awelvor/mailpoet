Bonsoir monsieur Thiriez,

L'adresse du serveur de mails semble être dans la plage : 109.234.163.0/24.
Aussi pourriez vous s'il vous plaît modifier l'enregistrement SPF suivant :

SPF
TXT
paroisses-plestin-ploumilliau-plouaret.catholique.fr.
v=spf1 +mx +a +ip4:109.234.164.198 +ip4:109.234.163.31 include:spf.mailjet.com include:spf.protection.outlook.com ~all
par :

SPF
TXT
paroisses-plestin-ploumilliau-plouaret.catholique.fr.

v=spf1 +mx +a +ip4:109.234.164.198 +ip4:109.234.163.0/24 include:spf.mailjet.com include:spf.protection.outlook.com ~all



Merci.
Cordialement.
Patrice Dronnier


Bonsoir Philippe,

ça ne fonctionne toujours pas....
L'IP du serveur de mail change, ce qui fait qu'il ne figure pas dans l'enregistrement SPF.
Il faut que je trouve le moyen de s'affranchir des @IP.
Bon week-end.
Amicalement.
Patrice
