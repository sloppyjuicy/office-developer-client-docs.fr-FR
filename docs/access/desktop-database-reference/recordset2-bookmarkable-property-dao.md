---
title: Recordset2.Bookmarkable Property (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 9c93d04d-ca10-acf5-122a-58625ed93424
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198125(v=office.15)
ms:contentKeyID: 48546601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052888
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6685523b9fb1a55dee924f7d700a91d3ce9d427b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873781"
---
# <a name="recordset2bookmarkable-property-dao"></a>Recordset2.Bookmarkable Property (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie une valeur qui indique si un objet **Recordset** prend en charge les signets, que vous pouvez définir à l'aide de la propriété **[Bookmark](recordset2-bookmark-property-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . Bookmarkable

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Vérifiez la valeur de la propriété **Bookmarkable** d'un objet **Recordset** avant de définir ou de vérifier la propriété **Bookmark**.

Pour les objets **Recordset** repose entièrement sur les tables de moteur de base de données Microsoft Access, la valeur de la propriété **Bookmarkable** est True et vous pouvez utiliser les signets. En revanche, il est possible que d'autres produits de base de données ne prennent pas en charge les signets. Ainsi, vous ne pouvez pas utiliser de signets dans un objet **Recordset** basé sur une table Paradox liée qui ne possède aucune clé primaire.

## <a name="example"></a>Exemple

Cet exemple montre comment les propriétés **Bookmark** et **Bookmarkable** permettent à un utilisateur de marquer un enregistrement d'un jeu d'enregistrements afin de pouvoir y revenir ultérieurement.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
