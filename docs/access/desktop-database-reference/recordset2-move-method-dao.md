---
title: Recordset2.Move Method (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ee1bf654df8cebbb936111d633262fd7418f58a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875342"
---
# <a name="recordset2move-method-dao"></a>Recordset2.Move Method (DAO)


**S’applique à**: Access 2013, Office 2013

Déplace l'enregistrement actif d'un objet **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . Move (***lignes***, ***signetdébut***)

*expression* Variable qui représente un objet **Recordset2** .

### <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Lignes</p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Entier long</strong></p></td>
<td><p>Nombre de lignes en fonction duquel l'enregistrement est déplacé. Si l'argument rows a une valeur supérieure à 0, l'enregistrement avance (vers la fin du fichier). Si l'argument rows a une valeur inférieure à 0, l'enregistrement recule (vers le début du fichier).</p></td>
</tr>
<tr class="even">
<td><p>Signetdébut</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Valeur identifiant un signet. Si vous spécifiez l'argument startbookmark, le déplacement s'opère par rapport à ce signet. Sinon, l'opération Move part de l'enregistrement actif.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si vous utilisez **Move** pour positionner le pointeur d'enregistrement actif avant le premier enregistrement, le pointeur d'enregistrement actif se déplace au début du fichier. Si l'objet **Recordset** ne contient pas d'enregistrements et que sa propriété **[BOF](recordset2-bof-property-dao.md)** a la valeur **True**, le recours à cette méthode pour faire reculer un enregistrement entraîne une erreur.

Si vous utilisez **Move** pour positionner le pointeur d'enregistrement actif après le dernier enregistrement, le pointeur d'enregistrement actif se déplace à la fin du fichier. Si l'objet **Recordset** ne contient pas d'enregistrements et que sa propriété **[EOF](recordset2-eof-property-dao.md)** a la valeur **True**, le recours à cette méthode pour faire avancer un enregistrement entraîne une erreur.

Si la propriété **BOF** ou **EOF** a la valeur **True** et que vous tentez d'utiliser la méthode **Move** sans un signet valide, une erreur d'exécution se produit.


> [!NOTE]
> <UL>
> <LI>
> <P>Lorsque vous appliquez la méthode <STRONG>Move</STRONG> à un objet <STRONG>Recordset</STRONG> de type avant uniquement, la valeur de l'argument « rows » doit être un entier positif et les signets ne sont pas autorisés. Cela signifie que vous pouvez uniquement faire avancer un enregistrement.</P>
> <LI>
> <P>Pour faire de l'enregistrement actif le premier enregistrement, le dernier, le suivant ou le précédent dans un objet <STRONG>Recordset</STRONG>, utilisez la méthode <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG> ou <STRONG>MovePrevious</STRONG>.</P>
> <LI>
> <P>Le fait d'utiliser la méthode <STRONG>Move</STRONG> en attribuant la valeur 0 à l'argument « rows » permet d'extraire facilement les données sous-jacentes de l'enregistrement actif. Cela peut vous être utile si vous souhaitez vous assurer que l'enregistrement actif comporte les données les plus récentes des tables de base. Cela permet également d'annuler les appels <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> ou <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> en cours.</P></LI></UL>



## <a name="example"></a>Exemple

Cet exemple de code montre comment utiliser la méthode **Move** pour positionner le pointeur d'enregistrement en fonction de l'entrée de l'utilisateur.

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
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
