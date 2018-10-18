---
<<<<<<< Titre tête : TOCTitle Type propriété (ADO) : Type de propriété (ADO) === titre : Type, propriété (ADO) TOCTitle : Type, propriété (ADO)
>>>>>>> Master ms:assetid : 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl : https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID : ms.date 48543397 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="type-property-ado"></a>Type, propriété (ADO)
=======
# <a name="type-property-ado"></a>Type, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le type opérationnel ou le type de données de l'objet [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur [DataTypeEnum](datatypeenum.md).

## <a name="remarks"></a>Remarques

La propriété **Type** est en lecture/écriture pour les objets **Parameter**. Pour les nouveaux objets **Field** ayant été ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Type** n'est accessible en lecture et en écriture qu'une fois que la propriété [Value](value-property-ado.md) de l'objet **Field** est spécifiée et que le fournisseur de données a correctement ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md) de la collection **Fields**.

Pour tous les autres objets, la propriété **Type** est en lecture seule.

