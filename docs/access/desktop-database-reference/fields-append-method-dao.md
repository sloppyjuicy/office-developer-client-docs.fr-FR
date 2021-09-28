---
title: Fields.Append, méthode (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: f233e85fd6de5b7bfb31b0e4e1211ce7612996af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618126"
---
# <a name="fieldsappend-method-dao"></a>Fields.Append, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Ajoute un nouveau **[champ](field-object-dao.md)** à la collection de sites **[Fields](fields-collection-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* .Append(***Object***)

*expression* Variable qui représente un objet **Fields**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Object</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Object</strong></p></td>
<td><p>Variable d'objet représentant le champ qui est ajouté à la collection.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser la méthode **Append** pour ajouter une table à une base de données, ajouter un champ à une table ou à un index.

L'objet ajouté devient un objet persistant, stocké sur le disque, tant que vous ne le supprimez pas à l'aide de la méthode **Delete**.

L'ajout d'un nouvel objet a lieu immédiatement, mais vous devez utiliser la méthode **Refresh** dans toutes les autres collections qui peuvent être affectées par les modifications apportées à la structure de la base de données.

Si l'objet que vous ajoutez n'est pas complet (par exemple, si vous n'avez pas ajouté d'objets **Field** à une collection **Fields** d'un objet **Index** avant son ajout à une collection **Indexes**) ou si les propriétés définies dans un ou plusieurs objets subordonnés sont incorrectes, l'utilisation de la méthode **Append** entraîne une erreur. Par exemple, si vous n'avez pas spécifié un type de champ et que vous tentez d'ajouter l'objet **Field** à la collection **Fields** dans un objet **TableDef** à l'aide de la méthode **Append**, une erreur d'exécution est générée.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **Append** ou la méthode **Delete** pour modifier la collection **Fields** d'une **TableDef**. La procédure AppendDeleteField est nécessaire à l'exécution de cette procédure.

```vb
    Sub AppendX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Add three new fields. 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "E-mail", dbText, 50 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Http", dbText, 80 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Quota", dbInteger, 5 
     
     Debug.Print "Fields after Append" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show the new fields. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     ' Delete the newly added fields. 
     AppendDeleteField tdfEmployees, "DELETE", "E-mail" 
     AppendDeleteField tdfEmployees, "DELETE", "Http" 
     AppendDeleteField tdfEmployees, "DELETE", "Quota" 
     
     Debug.Print "Fields after Delete" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show that the new 
     ' fields have been deleted. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub AppendDeleteField(tdfTemp As TableDef, _ 
     strCommand As String, strName As String, _ 
     Optional varType, Optional varSize) 
     
     With tdfTemp 
     
     ' Check first to see if the TableDef object is 
     ' updatable. If it isn't, control is passed back to 
     ' the calling procedure. 
     If .Updatable = False Then 
     MsgBox "TableDef not Updatable! " & _ 
     "Unable to complete task." 
     Exit Sub 
     End If 
     
     ' Depending on the passed data, append or delete a 
     ' field to the Fields collection of the specified 
     ' TableDef object. 
     If strCommand = "APPEND" Then 
     .Fields.Append .CreateField(strName, _ 
     varType, varSize) 
     Else 
     If strCommand = "DELETE" Then .Fields.Delete _ 
     strName 
     End If 
     
     End With 
     
    End Sub
```
