---
title: Méthode Recordset.Move (DAO)
TOCTitle: Move Method
ms:assetid: 21ca5ab5-ff71-1ae8-21b3-8991d5f795cf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191697(v=office.15)
ms:contentKeyID: 48543689
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052941
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1f10b5b779141189f114e420b3f7d4827e701161
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709662"
---
# <a name="recordsetmove-method-dao"></a>Méthode Recordset.Move (DAO)

**S’applique à**: Access 2013, Office 2013

Déplace l'enregistrement actif d'un objet **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . Move (***lignes***, ***signetdébut***)

*expression* Variable qui représente un objet **Recordset** .

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
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Entier long</strong></p></td>
<td><p>Nombre de lignes en fonction duquel l'enregistrement est déplacé. Si l'argument rows a une valeur supérieure à 0, l'enregistrement avance (vers la fin du fichier). Si l'argument rows a une valeur inférieure à 0, l'enregistrement recule (vers le début du fichier).</p></td>
</tr>
<tr class="even">
<td><p><em>Signetdébut</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Valeur identifiant un signet. Si vous spécifiez l'argument startbookmark, le déplacement s'opère par rapport à ce signet. Sinon, l'opération Move part de l'enregistrement actif.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si vous utilisez **Move** pour positionner le pointeur d'enregistrement actif avant le premier enregistrement, le pointeur d'enregistrement actif se déplace au début du fichier. Si l'objet **Recordset** ne contient pas d'enregistrements et que sa propriété **[BOF](recordset-bof-property-dao.md)** a la valeur **True**, le recours à cette méthode pour faire reculer un enregistrement entraîne une erreur.

Si vous utilisez **Move** pour positionner le pointeur d'enregistrement actif après le dernier enregistrement, le pointeur d'enregistrement actif se déplace à la fin du fichier. Si l'objet **Recordset** ne contient pas d'enregistrements et que sa propriété **[EOF](recordset-eof-property-dao.md)** a la valeur **True**, le recours à cette méthode pour faire avancer un enregistrement entraîne une erreur.

Si la propriété **BOF** ou **EOF** a la valeur **True** et que vous tentez d'utiliser la méthode **Move** sans un signet valide, une erreur d'exécution se produit.

> [!NOTE]
> - Lorsque vous appliquez la méthode **Move** à un objet **Recordset** de type avant uniquement, la valeur de l'argument « rows » doit être un entier positif et les signets ne sont pas autorisés. Cela signifie que vous pouvez uniquement faire avancer un enregistrement.
> - Pour faire de l'enregistrement actif le premier enregistrement, le dernier, le suivant ou le précédent dans un objet **Recordset**, utilisez la méthode **MoveFirst**, **MoveLast**, **MoveNext** ou **MovePrevious**.
> - Le fait d'utiliser la méthode **Move** en attribuant la valeur 0 à l'argument « rows » permet d'extraire facilement les données sous-jacentes de l'enregistrement actif. Cela peut vous être utile si vous souhaitez vous assurer que l'enregistrement actif comporte les données les plus récentes des tables de base. Cela permet également d'annuler les appels **[Edit](recordset2-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)** en cours.


## <a name="example"></a>Exemple

Cet exemple de code montre comment utiliser la méthode **Move** pour positionner le pointeur d'enregistrement en fonction de l'entrée de l'utilisateur.

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
