---
title: Recordset2.Bookmark, propriété (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31791e9fb3c7081989232e36a90b184ed7e31866
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307447"
---
# <a name="recordset2bookmark-property-dao"></a><span data-ttu-id="f972f-102">Recordset2.Bookmark, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="f972f-102">Recordset2.Bookmark property (DAO)</span></span>


<span data-ttu-id="f972f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f972f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f972f-104">Définit ou renvoie un signet qui identifie de façon unique l'enregistrement actif dans un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f972f-104">Sets or returns a bookmark that uniquely identifies the current record in a **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f972f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f972f-105">Syntax</span></span>

<span data-ttu-id="f972f-106">*expression* . Bookmark</span><span class="sxs-lookup"><span data-stu-id="f972f-106">*expression* .Bookmark</span></span>

<span data-ttu-id="f972f-107">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="f972f-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f972f-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="f972f-108">Remarks</span></span>

<span data-ttu-id="f972f-109">Pour un objet **Recordset** entièrement basé sur les tables du moteur de base de données Microsoft Access, la valeur de la propriété **Bookmarkable** est True et vous pouvez utiliser la propriété **Bookmark** avec ce jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="f972f-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use the **Bookmark** property with that recordset.</span></span> <span data-ttu-id="f972f-110">Il se peut que d'autres produits de base de données ne prennent pas en charge les signets.</span><span class="sxs-lookup"><span data-stu-id="f972f-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="f972f-111">Par exemple, vous ne pouvez pas utiliser de signets dans un objet **Recordset2** basé sur une table Paradox attachée, qui ne possède pas de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="f972f-111">For example, you can't use bookmarks in any **Recordset2** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="f972f-p102">Lorsque vous créez ou que vous ouvrez un objet **Recordset**, chacun de ses enregistrements possède un signet qui lui est propre. Vous pouvez enregistrer le signet de l'enregistrement actif en affectant à la propriété **Bookmark** une variable. Pour revenir rapidement et à tout moment à cet enregistrement après avoir accédé à un autre enregistrement, affectez à la propriété **Bookmark** de l'objet **Recordset** la valeur de cette variable.</span><span class="sxs-lookup"><span data-stu-id="f972f-p102">When you create or open a **Recordset** object, each of its records already has a unique bookmark. You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="f972f-p103">Il n'existe aucune limite quant au nombre de signets que vous pouvez définir. Pour créer un signet d'un enregistrement autre que l'enregistrement actif, accédez à l'enregistrement souhaité et affectez à la propriété **Bookmark** une variable de type **String** qui identifie l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f972f-p103">There is no limit to the number of bookmarks you can establish. To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="f972f-117">Pour vous assurer que l’objet **Recordset** prend en charge les signets, vérifiez la valeur de sa propriété **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** avant d’utiliser la propriété **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="f972f-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="f972f-118">Si la propriété **Bookmarkable** est False, l'objet **Recordset** ne prend pas en charge les signets et l'utilisation de la propriété **Bookmark** provoquera une erreur piégeable.</span><span class="sxs-lookup"><span data-stu-id="f972f-118">If the **Bookmarkable** property is False, the **Recordset** object doesn't support bookmarks, and using the **Bookmark** property results in a trappable error.</span></span>

<span data-ttu-id="f972f-p105">Si vous utilisez la méthode **[Clone](recordset2-clone-method-dao.md)** pour créer une copie de l'objet **Recordset**, les paramètres de la propriété **Bookmark** des objets **Recordset** d'origine et dupliqué sont identiques et interchangeables. En revanche, vous ne pouvez pas utiliser indifféremment des signets d'objets **Recordset** différents même s'ils ont été créés à l'aide du même objet ou de la même instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="f972f-p105">If you use the **[Clone](recordset2-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably. However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="f972f-121">Si vous affectez à la propriété **Bookmark** une valeur qui représente un enregistrement supprimé, une erreur piégeable se produit.</span><span class="sxs-lookup"><span data-stu-id="f972f-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="f972f-122">La valeur de la propriété **Bookmark** est différente d’un numéro d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f972f-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="f972f-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="f972f-123">Example</span></span>

<span data-ttu-id="f972f-124">Cet exemple montre comment les propriétés **Bookmark** et **Bookmarkable** permettent à un utilisateur de marquer un enregistrement d'un jeu d'enregistrements afin de pouvoir y revenir ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f972f-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

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

<span data-ttu-id="f972f-125">Cet exemple utilise la propriété **LastModified** pour déplacer le pointeur d'enregistrement actif sur un enregistrement modifié et sur un enregistrement récemment créé.</span><span class="sxs-lookup"><span data-stu-id="f972f-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

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
