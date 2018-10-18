---
<<<<<<< Titre tête : TOCTitle nombre propriété (ADO) : numéro de propriété (ADO) === titre : Number, propriété (ADO) TOCTitle : Number, propriété (ADO)
>>>>>>> Master ms:assetid : b5103af5-356b-ec74-cd62-86e59467d491 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249868(v=office.15) ms:contentKeyID : ms.date 48547243 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="number-property-ado"></a>Number, propriété (ADO)
=======
# <a name="number-property-ado"></a>Number, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le numéro qui identifie de manière unique un objet [Error](error-object-ado.md).

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie une valeur de type **Long** pouvant correspondre à l'une des constantes [ErrorValueEnum](errorvalueenum.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **Number** pour identifier l'erreur générée. La valeur de la propriété est un nombre unique qui correspond à la condition d'erreur.

La collection [Errors](errors-collection-ado.md) renvoie un HRESULT en format format hexadécimal (0x80004005 par exemple) ou une valeur longue (2147467259 par exemple). Ces HRESULT peuvent être déclenchés par composants sous-jacents comme OLE DB ou même OLE. Pour plus d’informations sur ces numéros, consultez le chapitre 16 de la *de référence du programmeur OLE DB.*

