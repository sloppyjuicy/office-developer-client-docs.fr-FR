---
title: Recordset2.Bookmark Property (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 46d349bb5b9061afa2f5df13b6a9da45e1b942a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469675"
---
# <a name="recordset2bookmark-property-dao"></a><span data-ttu-id="05f06-102">Recordset2.Bookmark Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="05f06-102">Recordset2.Bookmark Property (DAO)</span></span>


<span data-ttu-id="05f06-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="05f06-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="05f06-104">Définit ou renvoie un signet qui identifie de façon unique l'enregistrement actif dans un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="05f06-104">Sets or returns a bookmark that uniquely identifies the current record in a **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f06-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05f06-105">Syntax</span></span>

<span data-ttu-id="05f06-106">*expression* . Signet</span><span class="sxs-lookup"><span data-stu-id="05f06-106">*expression* .Bookmark</span></span>

<span data-ttu-id="05f06-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="05f06-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="05f06-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="05f06-108">Remarks</span></span>

<span data-ttu-id="05f06-109">Pour un objet **Recordset** est basé entièrement sur des tables de moteur de base de données Microsoft Access, la valeur de la propriété **Bookmarkable** est True et vous pouvez utiliser la propriété **Bookmark** avec ce jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="05f06-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use the **Bookmark** property with that recordset.</span></span> <span data-ttu-id="05f06-110">Il se peut que d'autres produits de base de données ne prennent pas en charge les signets.</span><span class="sxs-lookup"><span data-stu-id="05f06-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="05f06-111">Par exemple, vous ne pouvez pas utiliser de signets dans un objet **Recordset2** basé sur une table Paradox attachée, qui ne possède pas de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="05f06-111">For example, you can't use bookmarks in any **Recordset2** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="05f06-p102">Lors de la création ou de l'ouverture d'un objet **Recordset**, chacun de ses enregistrements contient déjà un signet unique. Vous pouvez enregistrer le signet de l'enregistrement actif en affectant la valeur de la propriété **Bookmark** à une variable. Pour revenir rapidement à cet enregistrement après être passé à un autre enregistrement, définissez la propriété **Bookmark** de l'objet **Recordset** sur la valeur de cette variable.</span><span class="sxs-lookup"><span data-stu-id="05f06-p102">When you create or open a **Recordset** object, each of its records already has a unique bookmark. You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="05f06-p103">Vous pouvez créer autant de signets que vous le souhaitez. Pour créer un signet pour un enregistrement différent de l'enregistrement actif, accédez à cet enregistrement et définissez comme paramètre de la propriété **Bookmark** une variable **String** qui identifie cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="05f06-p103">There is no limit to the number of bookmarks you can establish. To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="05f06-117">Pour vous assurer que l'objet **Recordset** prend en charge les signets, consultez la valeur de la propriété **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** avant d'utiliser la propriété **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="05f06-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="05f06-118">Si la propriété **Bookmarkable** est False, l’objet **Recordset** ne prend pas en charge les signets, et à l’aide du **signet** de la propriété génère une erreur interceptable.</span><span class="sxs-lookup"><span data-stu-id="05f06-118">If the **Bookmarkable** property is False, the **Recordset** object doesn't support bookmarks, and using the **Bookmark** property results in a trappable error.</span></span>

<span data-ttu-id="05f06-p105">Si vous créez une copie d'un objet [Recordset](recordset2-clone-method-dao.md) à l'aide de la méthode \*\*\*\*Clone\*\*\*\*, les valeurs de la propriété **Bookmark** correspondant aux objets **Recordset** d'origine et dupliqué sont identiques et peuvent être utilisées indifféremment. Toutefois, vous ne pouvez pas utiliser indifféremment les signets d'objets **Recordset** différents, même s'ils ont été créés à l'aide du même objet ou de la même instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="05f06-p105">If you use the **[Clone](recordset2-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably. However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="05f06-121">Une erreur interceptable se produit si vous définissez la propriété **Bookmark** sur une valeur qui représente un enregistrement supprimé.</span><span class="sxs-lookup"><span data-stu-id="05f06-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="05f06-122">La valeur de la propriété **Bookmark** est différente d'un numéro d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="05f06-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="05f06-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="05f06-123">Example</span></span>

<span data-ttu-id="05f06-124">Cet exemple montre comment les propriétés **Bookmark** et **Bookmarkable** permettent à un utilisateur de marquer un enregistrement d'un jeu d'enregistrements afin de pouvoir y revenir ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="05f06-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

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

<span data-ttu-id="05f06-125">Cet exemple utilise la propriété **LastModified** pour déplacer le pointeur d'enregistrement actif sur un enregistrement modifié et sur un enregistrement récemment créé.</span><span class="sxs-lookup"><span data-stu-id="05f06-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

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
