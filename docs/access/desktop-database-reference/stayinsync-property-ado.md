---
<<<<<<< Titre tête : TOCTitle StayInSync propriété (ADO) : propriété StayInSync (ADO) === titre : StayInSync, propriété (ADO) TOCTitle : StayInSync, propriété (ADO)
>>>>>>> Master ms:assetid : 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl : https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID : ms.date 48542966 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="stayinsync-property-ado"></a>StayInSync, propriété (ADO)
=======
# <a name="stayinsync-property-ado"></a>StayInSync, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique, dans un objet [Recordset](recordset-object-ado.md) hiérarchique, si la référence aux enregistrements enfants sous-jacents (c'est-à-dire, le *chapitre*) change en même temps que la position de la ligne parente.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **Boolean**. La valeur par défaut est **True**. Avec une valeur **True**, le chapitre est mis à jour lorsque l'objet **Recordset** parent change de position de ligne ; en cas de valeur **False**, le chapitre continue à faire référence aux données du chapitre précédent même si l'objet **Recordset** parent a changé de position de ligne.

## <a name="remarks"></a>Remarques

Cette propriété s'applique aux objets Recordset hiérarchiques, comme ceux pris en charge par [Microsoft Data Shaping Service pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) et doit être définie sur le **Recordset** parent avant que le **Recordset** ne soit extrait. Cette propriété simplifie la navigation dans les jeux d'enregistrements hiérarchiques.

