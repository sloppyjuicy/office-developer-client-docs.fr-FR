---
<<<<<<< Titre tête : MarshalOptions propriété (ADO) TOCTitle : MarshalOptions propriété (ADO) === titre : MarshalOptions, propriété (ADO) TOCTitle : MarshalOptions, propriété (ADO)
>>>>>>> Master ms:assetid : dc9c4e94-0725-210d-8251-079054541142 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250118(v=office.15) ms:contentKeyID : ms.date 48548143 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="marshaloptions-property-ado"></a>MarshalOptions, propriété (ADO)
=======
# <a name="marshaloptions-property-ado"></a>MarshalOptions, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique les enregistrements dont les paramètres doivent être convertis avant d'être renvoyés vers le serveur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

Définit ou renvoie une valeur [MarshalOptions](marshaloptionsenum.md). La valeur par défaut est **adMarshalAll**.

## <a name="remarks"></a>Remarques

<<<<<<< Tête lors de l’utilisation d’un [jeu d’enregistrements](recordset-object-ado.md)du côté client, les enregistrements qui ont été modifiés sur le client sont réécrits au niveau intermédiaire ou au serveur Web via une technique appelée marshaling, le processus d’empaquetage et de l’envoi d’interface paramètres de méthode au-delà des limites de thread ou un processus. La définition de la propriété **MarshalOptions** peut améliorer les performances lorsque les paramètres des données distantes modifiées sont convertis pour être mis à jour sur le niveau intermédiaire ou le serveur Web.
=== Lorsque vous utilisez un [jeu d’enregistrements](recordset-object-ado.md)du côté client, les enregistrements qui ont été modifiés sur le client sont réécrits au niveau intermédiaire ou au serveur web via une technique appelée marshaling, le processus d’empaquetage et d’envoi des paramètres de méthode d’interface entre limites de thread ou un processus. Définition de la propriété **MarshalOptions** peut améliorer les performances lors du marshaling de données distantes modifiées pour mettre à jour au niveau intermédiaire ou au serveur web.
>>>>>>> master

**L’utilisation du Service de données à distance** Cette propriété est utilisée uniquement sur un **jeu d’enregistrements**du côté client.

