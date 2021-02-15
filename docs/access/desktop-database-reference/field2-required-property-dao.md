---
title: Field2.Required, propriété (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6b1950c8a864fbf23bee26be89e07e49357840b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292719"
---
# <a name="field2required-property-dao"></a>Field2.Required, propriété (DAO)


**S’applique à** : Access 2013, Office 2013


Définit ou renvoie une valeur qui indique si un objet **Field2** requiert une valeur non nulle.

## <a name="syntax"></a>Syntaxe

*.* Obligatoire

*expression* une variable qui représente une **champ2** objet.

## <a name="remarks"></a>Remarques

Pour un objet **Field2** pas encore ajouté à la collection **Fields**, cette propriété est en lecture/écriture.

La disponibilité de la propriété **Required** dépend de l'objet contenant la collection **[Fields](fields-collection-dao.md)**, comme illustré dans le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si la collection Fields appartient à un</p></th>
<th><p>Alors Required est</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>objet <strong>Index</strong></p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>Relation</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>TableDef</strong></p></td>
<td><p>Lecture/écriture</p></td>
</tr>
</tbody>
</table>


Vous pouvez utiliser la propriété **Required** avec les propriétés **AllowZeroLength**, **ValidateOnSet** ou **ValidationRule** pour déterminer la validité du paramètre de propriété **Value** pour cet objet **Field2**. Si la propriété **Required** est définie sur **False**, le champ peut contenir des valeurs de type **null** et des valeurs répondant aux conditions spécifiées par les paramètres de propriété **AllowZeroLength** et **ValidationRule**.


> [!NOTE]
> [!REMARQUE] Lorsque vous définissez cette propriété pour un objet **Index** ou **Field2**, définissez-la pour l'objet **Field2**. La validité du paramètre de propriété d'un objet **Field2** est vérifiée avant celle d'un objet **Index**.



## <a name="example"></a>Exemple

Cet exemple utilise la propriété **Required** pour signaler les champs de trois tables différentes à renseigner obligatoirement pour ajouter un nouvel enregistrement. La fonction RequiredOutput est indispensable pour l'exécution de cette procédure.

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

