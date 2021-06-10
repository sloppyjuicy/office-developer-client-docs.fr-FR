---
title: Recordset.Bookmarkable, propriété (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bd9b91f80c9411bb7cdf4e0be9e71ab055dc72f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300622"
---
# <a name="recordsetbookmarkable-property-dao"></a><span data-ttu-id="cbd61-102">Recordset.Bookmarkable, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="cbd61-102">Recordset.Bookmarkable property (DAO)</span></span>


<span data-ttu-id="cbd61-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbd61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbd61-104">Renvoie une valeur qui indique si un objet **Recordset** prend en charge les signets, pouvant être défini en utilisant la propriétéSignet.</span><span class="sxs-lookup"><span data-stu-id="cbd61-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd61-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbd61-105">Syntax</span></span>

<span data-ttu-id="cbd61-106">*.* Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="cbd61-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="cbd61-107">*expression* Variable qui représente un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="cbd61-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbd61-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="cbd61-108">Remarks</span></span>

<span data-ttu-id="cbd61-109">Vérifiez le paramètre de la propriété **Bookmarkable** d'un objet **Recordset** avant de tenter de définir ou contrôler la propriété **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="cbd61-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="cbd61-110">Pour les objets **Recordset** entièrement basés sur les tables du moteur de base de données Microsoft Access, la valeur de la propriété **Bookmarkable** est True et vous pouvez utiliser des signets.</span><span class="sxs-lookup"><span data-stu-id="cbd61-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="cbd61-111">En revanche, il est possible que d'autres produits de base de données ne prennent pas en charge les signets.</span><span class="sxs-lookup"><span data-stu-id="cbd61-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="cbd61-112">Ainsi, vous ne pouvez pas utiliser de signets dans un objet **Recordset** basé sur une table Paradox liée qui ne possède aucune clé primaire.</span><span class="sxs-lookup"><span data-stu-id="cbd61-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="cbd61-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="cbd61-113">Example</span></span>

<span data-ttu-id="cbd61-114">Cet exemple utilise les propriétés **Bookmark** et **Bookmarkable** pour permettre à l’utilisateur de marquer un enregistrement dans un jeu **Recordset** et d’y revenir plus tard.</span><span class="sxs-lookup"><span data-stu-id="cbd61-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

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
