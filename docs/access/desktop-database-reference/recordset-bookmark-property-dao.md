---
title: Recordset.Bookmark Property (DAO)
TOCTitle: Bookmark Property
ms:assetid: c4b1c2d9-668e-e365-544c-efb4ae4efcc9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823084(v=office.15)
ms:contentKeyID: 48547597
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052887
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 644eb2e1a8f979451d233bcc5a48f723c25739b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888474"
---
# <a name="recordsetbookmark-property-dao"></a>Recordset.Bookmark Property (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie un signet qui identifie de façon unique l'enregistrement actif d'un objet **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . Signet

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Pour un objet **Recordset** est basé entièrement sur des tables de moteur de base de données Microsoft Access, la valeur de la propriété **Bookmarkable** est True et vous pouvez utiliser la propriété **Bookmark** avec ce **jeu d’enregistrements**. En revanche, il est possible que d'autres produits de base de données ne prennent pas en charge les signets. Ainsi, vous ne pouvez pas utiliser de signets dans un objet **Recordset** basé sur une table Paradox liée qui ne possède aucune clé primaire.

Lors de la création ou de l'ouverture d'un objet **Recordset**, chacun de ses enregistrements contient déjà un signet unique. Vous pouvez enregistrer le signet de l'enregistrement actif en affectant la valeur de la propriété **Bookmark** à une variable. Pour revenir rapidement à cet enregistrement après être passé à un autre enregistrement, définissez la propriété **Bookmark** de l'objet **Recordset** sur la valeur de cette variable.

Vous pouvez créer autant de signets que vous le souhaitez. Pour créer un signet pour un enregistrement différent de l'enregistrement actif, accédez à cet enregistrement et définissez comme paramètre de la propriété **Bookmark** une variable **String** qui identifie cet enregistrement.

Pour vous assurer que l'objet **Recordset** prend en charge les signets, consultez la valeur de la propriété **[Bookmarkable](recordset-bookmarkable-property-dao.md)** avant d'utiliser la propriété **Bookmark**. Si la propriété **Bookmarkable** est False, l’objet **Recordset** ne prend pas en charge les signets, et à l’aide du **signet** de la propriété génère une erreur interceptable.

Si vous créez une copie d'un objet [Recordset](recordset-clone-method-dao.md) à l'aide de la méthode ****Clone****, les valeurs de la propriété **Bookmark** correspondant aux objets **Recordset** d'origine et dupliqué sont identiques et peuvent être utilisées indifféremment. Toutefois, vous ne pouvez pas utiliser indifféremment les signets d'objets **Recordset** différents, même s'ils ont été créés à l'aide du même objet ou de la même instruction SQL.

Une erreur interceptable se produit si vous définissez la propriété **Bookmark** sur une valeur qui représente un enregistrement supprimé.

La valeur de la propriété **Bookmark** est différente d'un numéro d'enregistrement.

## <a name="example"></a>Exemple

L'exemple ci-dessous fait appel aux propriétés **Bookmark** et **Bookmarkable** pour permettre de marquer un enregistrement d'un objet **Recordset** et d'y revenir ultérieurement.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
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
     Dim rstEmployees As Recordset 
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
