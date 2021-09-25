---
title: Recordset2.Bookmark, propriété (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 79067ba0d5fc46b83de5a8d38bb174279f773b12
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597001"
---
# <a name="recordset2bookmark-property-dao"></a>Recordset2.Bookmark, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie un signet qui identifie de façon unique l'enregistrement actif dans un objet **Recordset**.

## <a name="syntax"></a>Syntaxe

*expression* . Bookmark

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Pour un objet **Recordset** entièrement basé sur les tables du moteur de base de données Microsoft Access, la valeur de la propriété **Bookmarkable** est True et vous pouvez utiliser la propriété **Bookmark** avec ce jeu d’enregistrements. Il se peut que d'autres produits de base de données ne prennent pas en charge les signets. Par exemple, vous ne pouvez pas utiliser de signets dans un objet **Recordset2** basé sur une table Paradox attachée, qui ne possède pas de clé primaire.

Lorsque vous créez ou que vous ouvrez un objet **Recordset**, chacun de ses enregistrements possède un signet qui lui est propre. Vous pouvez enregistrer le signet de l'enregistrement actif en affectant à la propriété **Bookmark** une variable. Pour revenir rapidement et à tout moment à cet enregistrement après avoir accédé à un autre enregistrement, affectez à la propriété **Bookmark** de l'objet **Recordset** la valeur de cette variable.

Il n'existe aucune limite quant au nombre de signets que vous pouvez définir. Pour créer un signet d'un enregistrement autre que l'enregistrement actif, accédez à l'enregistrement souhaité et affectez à la propriété **Bookmark** une variable de type **String** qui identifie l'enregistrement.

Pour vous assurer que l’objet **Recordset** prend en charge les signets, vérifiez la valeur de sa propriété **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** avant d’utiliser la propriété **Bookmark**. Si la propriété **Bookmarkable** est False, l'objet **Recordset** ne prend pas en charge les signets et l'utilisation de la propriété **Bookmark** provoquera une erreur piégeable.

Si vous utilisez la méthode **[Clone](recordset2-clone-method-dao.md)** pour créer une copie de l'objet **Recordset**, les paramètres de la propriété **Bookmark** des objets **Recordset** d'origine et dupliqué sont identiques et interchangeables. En revanche, vous ne pouvez pas utiliser indifféremment des signets d'objets **Recordset** différents même s'ils ont été créés à l'aide du même objet ou de la même instruction SQL.

Si vous affectez à la propriété **Bookmark** une valeur qui représente un enregistrement supprimé, une erreur piégeable se produit.

La valeur de la propriété **Bookmark** est différente d’un numéro d’enregistrement.

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

<br/>

Cet exemple utilise la propriété **LastModified** pour déplacer le pointeur d'enregistrement actif sur un enregistrement modifié et sur un enregistrement récemment créé.

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
