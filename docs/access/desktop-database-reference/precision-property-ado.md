---
<<<<<<< Titre tête : TOCTitle précision propriété (ADO) : précision propriété (ADO) === titre :, propriété (ADO) de la précision TOCTitle : propriété précision (ADO)
>>>>>>> Master ms:assetid : c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID : ms.date 48547685 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="precision-property-ado"></a>Precision, propriété (ADO)
=======
# <a name="precision-property-ado"></a>Precision, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le degré de précision des valeurs numériques d'un objet [Parameter](parameter-object-ado.md) ou d'un objet [Field](field-object-ado.md) numérique.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **Byte** qui indique le nombre maximal de chiffres utilisés pour représenter les valeurs.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Précision** pour déterminer le nombre maximal de chiffres utilisés pour représenter les valeurs d'un objet **Parameter** ou **Field** numérique.

Sur un objet **Parameter** cette valeur est accessible lecture/écriture.

Pour un objet **Field**, **Precision** est généralement en lecture seule. Toutefois, pour les objets **Field** récemment ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), **Precision** est exceptionnellement accessible en lecture et en écriture après la définition de la propriété [Value](value-property-ado.md) de l'objet **Field** et une fois que le fournisseur de données a ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md) de la collection **Fields**.

