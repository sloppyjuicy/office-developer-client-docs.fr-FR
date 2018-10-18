---
<<<<<<< Titre tête : propriété MaxRecords (ADO) TOCTitle : propriété MaxRecords (ADO) === titre : MaxRecords, propriété (ADO) TOCTitle : MaxRecords, propriété (ADO)
>>>>>>> Master ms:assetid : 424b2d41-073a-3fbe-30aa-99fac94f9a81 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249195(v=office.15) ms:contentKeyID : ms.date 48544475 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="maxrecords-property-ado"></a>MaxRecords, propriété (ADO)
=======
# <a name="maxrecords-property-ado"></a>MaxRecords, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le nombre maximum d'enregistrements à renvoyer à un [Recordset](recordset-object-ado.md) après une requête.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **Long** qui indique le nombre maximum d'enregistrements à renvoyer. La valeur par défaut est zéro (pas de limite).

## <a name="remarks"></a>Remarques

Utilisez la propriété **MaxRecords** pour limiter le nombre d'enregistrements de la source de données que le fournisseur doit renvoyer. Le paramètre par défaut de cette propriété est zéro, ce qui signifie que le fournisseur renvoie tous les enregistrements demandés.

La propriété **MaxRecords** est accessible en lecture/écriture lorsque le **Recordset** est fermé et en lecture seule lorsqu'il est ouvert.

