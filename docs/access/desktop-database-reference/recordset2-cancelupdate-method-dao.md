---
title: Recordset2.CancelUpdate, méthode (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 17c9986bbd69501b20b02e0e9c5e3615e0e2125e
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634981"
---
# <a name="recordset2cancelupdate-method-dao"></a>Recordset2.CancelUpdate, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Annule les mises à jour en attente pour un objet **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*.* CancelUpdate(***UpdateType***)

*expression* Variable qui représente un **objet Recordset2** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
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
<td><p>Définissez cette propriété sur l’une <strong><a href="updatetypeenum-enumeration-dao.md">des valeurs UpdateTypeEnum</a></strong> .</p><p><strong>REMARQUE</strong> : les <EM>valeurs dbUpdateRegular</EM> et <EM>dbUpdateBatch</EM> ne sont valides que si la mise à jour par lot est activée.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser la méthode **CancelUpdate** pour annuler les mises à jour en attente résultant d'une opération **[Edit](recordset2-edit-method-dao.md)** ou **[AddNew](recordset2-addnew-method-dao.md)**. Par exemple, si un utilisateur appelle la méthode **Edit** ou **AddNew** alors qu'il n'a pas encore appelé la méthode **Update**, **CancelUpdate** annule les modifications apportées consécutivement à l'appel de **Edit** ou **AddNew**.

Vérifiez la propriété **[EditMode](recordset2-editmode-property-dao.md)** de l'objet **Recordset** pour déterminer s'il existe une opération en attente susceptible d'être annulée.

> [!NOTE]
> [!REMARQUE] Le fait d'utiliser la méthode **CancelUpdate** revient à atteindre un autre enregistrement sans utiliser la méthode **[Update](recordset2-update-method-dao.md)**, à ceci près que l'enregistrement actif ne change pas et que plusieurs propriétés, telles que **[BOF](recordset2-bof-property-dao.md)** et **[EOF](recordset2-eof-property-dao.md)**, ne sont pas mises à jour.

## <a name="example"></a>Exemple

Cet exemple de code montre comment utiliser la méthode **CancelUpdate** avec la méthode **AddNew**.

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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

