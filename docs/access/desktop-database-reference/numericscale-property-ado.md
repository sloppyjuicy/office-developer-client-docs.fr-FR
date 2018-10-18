---
<<<<<<< Titre tête : TOCTitle NumericScale propriété (ADO) : propriété NumericScale (ADO) === titre : NumericScale, propriété (ADO) TOCTitle : NumericScale, propriété (ADO)
>>>>>>> Master ms:assetid : 51b232d2-5bfd-521c-f4e9-65655ecc7c70 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249263(v=office.15) ms:contentKeyID : ms.date 48544824 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="numericscale-property-ado"></a>NumericScale, propriété (ADO)
=======
# <a name="numericscale-property-ado"></a>NumericScale, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique l'échelle des valeurs numériques possibles dans un objet [Parameter](parameter-object-ado.md) ou [Field](field-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **Byte** qui indique le nombre de décimales que comporteront les valeurs numériques.

## <a name="remarks"></a>Remarques

Utilisez la propriété **NumericScale** pour déterminer combien de chiffres à droite de la virgule seront utilisés pour représenter les valeurs d'un objet **Parameter** ou **Field** numérique.

Pour les objets **Parameter**, la propriété **NumericScale** est accessible en lecture et écriture.

Pour un objet **Field**, **NumericScale** est généralement en lecture seule. Toutefois, pour les objets **Field** récemment ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), **NumericScale** est exceptionnellement accessible en lecture et en écriture après la définition de la propriété [Value](value-property-ado.md) de l'objet **Field** et une fois que le fournisseur de données a ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md)de la collection **Fields**.

