---
title: Field.Required Property (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bfa474a1fd8b592f8ad8d309526c8b94cb1fba25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471651"
---
# <a name="fieldrequired-property-dao"></a>Field.Required Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Définit ou renvoie une valeur qui indique si un objet **[Field](field-object-dao.md)** requiert une valeur non Null.

## <a name="syntax"></a>Syntaxe

*expression* . Obligatoire

*expression* Variable qui représente un objet **Field** .

## <a name="remarks"></a>Remarques

Pour un objet **Field** qui n'a pas encore été ajouté à la collection **Fields**, cette propriété est en lecture-écriture.

La disponibilité de la propriété **Required** dépend de l'objet qui contient la collection [Fields](fields-collection-dao.md), comme indiqué dans le tableau ci-dessous.

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
<td><p>							objet <strong>Index</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td><p>							objet <strong>QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p>							objet <strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p>							objet <strong>Relation</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td><p>							objet <strong>TableDef</strong></p></td>
<td><p>En lecture-écriture.</p></td>
</tr>
</tbody>
</table>


Vous pouvez utiliser la propriété **Required** avec la propriété **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** ou **[ValidationRule](field-validationrule-property-dao.md)** pour déterminer la validité du paramètre de la propriété **[Value](field-value-property-dao.md)** de cet objet **Field**. Si la propriété **Required** a la valeur **False**, le champ peut contenir des valeurs **null** ainsi que des valeurs répondant aux conditions spécifiées par les paramètres des propriétés **AllowZeroLength** et **ValidationRule**.


> [!NOTE]
> <P>[!REMARQUE] Lorsque vous pouvez définir cette propriété pour un objet <STRONG>Index</STRONG> ou un objet <STRONG>Field</STRONG>, définissez-la pour l'objet <STRONG>Field</STRONG>. En effet, la validité du paramètre de la propriété d'un objet <STRONG>Field</STRONG> est vérifiée avant celle d'un objet <STRONG>Index</STRONG>.</P>



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
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

