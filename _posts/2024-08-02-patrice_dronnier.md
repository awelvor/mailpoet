Subject:	configuration DKIM et SPF mailpoet pour paroisses-plestin-ploumilliau-plouaret.catholique.fr
Date:	Fri, 2 Aug 2024 23:01:32 +0200
From:	Patrice Dronnier <patrice.dronnier@wanadoo.fr>
To:	hebergement@cef.fr

Bonsoir,

Sur le site web/domaine url : paroisses-plestin-ploumilliau-plouaret.catholique.fr, nous utilisons mailpoet pour l'abonnement de nos visiteurs à la lettre infos.
Mailpoet a été configuré pour envoyer les e-mails de la newsletter via l'hébergeur o2switch. J'ai effectué un test d'envoi de e-mail de newsletter via mailpoet qui fonctionne hormis que le e-mail atterrit dans mon dossier spam. L'expéditeur de la newsletter est le suivant : contact@paroisses-plestin-ploumilliau-plouaret.catholique.fr

Mailpoet indique qu'il faut ajouter au domaine DNS les enregistrements suivants (voir copie d'écran et tableau ci-dessous) :

CNAME
mailpoet1._domainkey.paroisses-plestin-ploumilliau-plouaret.catholique.fr
dkim1.sendingservice.net
CNAME
mailpoet2._domainkey.paroisses-plestin-ploumilliau-plouaret.catholique.fr
dkim2.sendingservice.net
TXT
_mailpoet.paroisses-plestin-ploumilliau-plouaret.catholique.fr
e15de31a3f065d7183a3a44d3d573cb2
TXT
_dmarc.paroisses-plestin-ploumilliau-plouaret.catholique.fr
v=DMARC1; p=none; rua=mailto:postmaster@catholique.fr; sp=none; fo=1; ri=86400; adkim=r; aspf=r

Sur le cpanel de o2switch dans le menu "Email deliverability", le Email deliverability status de paroisses-plestin-ploumilliau-plouaret.catholique.fr vaut " Problems Exist (DKIM et SPF)". L'outil suggère d'ajouter les enregistrements suivants (voir copie d'écran et tableau ci-dessous):

DKIM
TXT
default._domainkey.paroisses-plestin-ploumilliau-plouaret.catholique.fr.
v=DKIM1; k=rsa; p=MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAy8TOvaOun4EiC3ZBBcq1E/ysfnoZHpmfJoF2WUKu+zivTxfn3zHsj7O65P+L+GDp9tpB69pOsbjxS9UWv6u6QOjVX3UHnE5gIJpTlmDPC5OLD4IRD3eI3E+iE+UbbOJ2d7/ujaGBnYoMNL/0+lZAX1Ya8rANoCN06fWyONMHFdzr0hsQar1OjzzJt1jsK7OKADp3OGRYmb8ruVFN3evyMZdLyevSCA3ldI2iyC5cZ0DErsWt2ol1NBoly5WsMkyoh5TXonioN4CIz3xmV0ajK4L19GLpwBJjfS1KYBMcFeuu7zvYkTcrDeSS9dVUXG9FM3yJT8DsIGQWlO0Y9XVzvQIDAQAB;
SPF
TXT
paroisses-plestin-ploumilliau-plouaret.catholique.fr.
v=spf1 +mx +a +ip4:109.234.164.198 +ip4:109.234.163.31 include:spf.mailjet.com include:spf.protection.outlook.com ~all
Je ne sais pas s'il faut ajouter les 2 ensembles d'enregistrements au DNS catholique.fr pour résoudre ce problème d'authentification de l'expéditeur.
Avez-vous déjà eu à traiter ce problème de newsletter qui atterrit dans le dossier spam ?
SI oui, est-ce que vous pouvez m'aider s'il vous plaît ?
Merci pour votre aide.
Je vous souhaite un bon week-end.
Cordialement.
