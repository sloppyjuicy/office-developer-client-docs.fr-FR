---
title: Recordset.CancelUpdate, méthode (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5950154d8896678889af01254104a2ac0dfef4cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300678"
---
# <a name="recordsetcancelupdate-method-dao"></a>Recordset.CancelUpdate, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Annule les mises à jour en attente pour un objet **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*.* CancelUpdate(***UpdateType***)

*expression* Variable qui représente un objet **Recordset**.

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
<td><p><em>UpdateType</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Définissez cette propriété sur l’une <strong><a href="updatetypeenum-enumeration-dao.md">des valeurs UpdateTypeEnum.</a></strong></p><p><strong>REMARQUE</strong>: les <EM>valeurs dbUpdateRegular</EM> et <EM>dbUpdateBatch</EM> ne sont valides que si la mise à jour par lot est activée.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser la méthode **CancelUpdate** pour annuler les mises à jour en attente résultant d'une opération **[Edit](recordset-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)**. Par exemple, si un utilisateur appelle la méthode **Edit** ou **AddNew** alors qu'il n'a pas encore appelé la méthode **Update**, **CancelUpdate** annule les modifications apportées consécutivement à l'appel de **Edit** ou **AddNew**.

Vérifiez la propriété **[EditMode](recordset-editmode-property-dao.md)** de l'objet **Recordset** pour déterminer s'il existe une opération en attente susceptible d'être annulée.

> [!NOTE]
> [!REMARQUE] Le fait d'utiliser la méthode **CancelUpdate** revient à atteindre un autre enregistrement sans utiliser la méthode **[Update](recordset-update-method-dao.md)**, à ceci près que l'enregistrement actif ne change pas et que plusieurs propriétés, telles que **[BOF](recordset-bof-property-dao.md)** et **[EOF](recordset-eof-property-dao.md)**, ne sont pas mises à jour.


## <a name="example"></a>Exemple

Cet exemple de code montre comment utiliser la méthode **CancelUpdate** avec la méthode **AddNew**.

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Cet exemple de code montre comment utiliser la méthode **CancelUpdate** avec la méthode **Edit**.

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

