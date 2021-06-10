---
title: Recordset2.Bookmarkable, propriété (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 26b8b60255b4e50a2288dedb8e27906476926e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307454"
---
# <a name="recordset2bookmarkable-property-dao"></a><span data-ttu-id="9ad2c-102">Recordset2.Bookmarkable, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ad2c-102">Recordset2.Bookmarkable property (DAO)</span></span>


<span data-ttu-id="9ad2c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ad2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ad2c-104">Renvoie une valeur qui indique si un objet **Recordset** prend en charge les signets, pouvant être défini en utilisant la propriétéSignet.</span><span class="sxs-lookup"><span data-stu-id="9ad2c-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad2c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ad2c-105">Syntax</span></span>

<span data-ttu-id="9ad2c-106">*.* Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="9ad2c-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="9ad2c-107">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="9ad2c-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ad2c-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ad2c-108">Remarks</span></span>

<span data-ttu-id="9ad2c-109">Vérifiez le paramètre de la propriété **Bookmarkable** d'un objet **Recordset** avant de tenter de définir ou contrôler la propriété **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="9ad2c-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="9ad2c-110">Pour les objets **Recordset** entièrement basés sur les tables du moteur de base de données Microsoft Access, la valeur de la propriété **Bookmarkable** est True et vous pouvez utiliser des signets.</span><span class="sxs-lookup"><span data-stu-id="9ad2c-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="9ad2c-111">En revanche, il est possible que d'autres produits de base de données ne prennent pas en charge les signets.</span><span class="sxs-lookup"><span data-stu-id="9ad2c-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="9ad2c-112">Ainsi, vous ne pouvez pas utiliser de signets dans un objet **Recordset** basé sur une table Paradox liée qui ne possède aucune clé primaire.</span><span class="sxs-lookup"><span data-stu-id="9ad2c-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="9ad2c-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="9ad2c-113">Example</span></span>

<span data-ttu-id="9ad2c-114">Cet exemple montre comment les propriétés **Bookmark** et **Bookmarkable** permettent à un utilisateur de marquer un enregistrement d'un jeu d'enregistrements afin de pouvoir y revenir ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="9ad2c-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

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
