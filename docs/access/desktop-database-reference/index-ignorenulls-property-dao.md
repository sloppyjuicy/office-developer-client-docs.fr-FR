---
title: Propriété index. IgnoreNulls (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6c306f76e34e24abb5065c627d9325b48c3acead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291802"
---
# <a name="indexignorenulls-property-dao"></a>Propriété index. IgnoreNulls (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique si les enregistrements ayant des valeurs nulles dans leurs champs d’index ont des entrées d’index (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . IgnoreNulls

*expression* Variable qui représente un objet **index** .

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture pour un nouvel objet **[Index](index-object-dao.md)** pas encore ajouté à une collection et en lecture seule pour un objet **Index** existant de la collection **[Indexes](indexes-collection-dao.md)**.

Pour accélérer le processus de recherche des enregistrements, vous pouvez définir un index pour un champ. Si vous autorisez les entrées de type **null** dans un champ indexé et prévoyez d'avoir beaucoup d'entrées **null**, vous pouvez définir la propriété **IgnoreNulls** de l'objet **Index** sur **True** pour réduire la quantité d'espace de stockage utilisé par l'index.

Les paramètres de propriété **IgnoreNulls** et **[Required](field-required-property-dao.md)** déterminent ensemble si un enregistrement doté d'une valeur d'index de type **null** a une entrée d'index.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si IgnoreNulls est</p></th>
<th><p>Et Required est</p></th>
<th><p>Then</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>True</p></td>
<td><p>False</p></td>
<td><p>Une valeur nulle est autorisée dans le champ d'index ; aucune entrée d'index n'est ajoutée.</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>False</p></td>
<td><p>Une valeur nulle est autorisée dans le champ d'index ; entrée d'index ajoutée.</p></td>
</tr>
<tr class="odd">
<td><p>True ou False</p></td>
<td><p>True</p></td>
<td><p>Aucune valeur nulle n'est autorisée dans le champ d'index ; aucune entrée d'index n'est ajoutée.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Exemple

Cet exemple définit la propriété **IgnoreNulls** d'un nouvel **Index** sur **True** ou **False** en fonction de l'entrée de l'utilisateur, puis en démontre l'effet sur un **Recordset** contenant un enregistrement dont le champ de clé contient une valeur **Null**.

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
