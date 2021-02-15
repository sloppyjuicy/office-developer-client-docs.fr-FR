---
title: Recordset2.Clone, méthode (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6780a27d573f5ff7ff41060074fb8abb9f8e2b80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307391"
---
# <a name="recordset2clone-method-dao"></a><span data-ttu-id="e515c-102">Recordset2.Clone, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="e515c-102">Recordset2.Clone method (DAO)</span></span>

<span data-ttu-id="e515c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e515c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e515c-104">Crée un objet **[Recordset](recordset-object-dao.md)** en double qui fait référence à l'objet **Recordset2** d'origine.</span><span class="sxs-lookup"><span data-stu-id="e515c-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e515c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e515c-105">Syntax</span></span>

<span data-ttu-id="e515c-106">*expression* . Clone</span><span class="sxs-lookup"><span data-stu-id="e515c-106">*expression* .Clone</span></span>

<span data-ttu-id="e515c-107">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="e515c-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="e515c-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e515c-108">Return value</span></span>

<span data-ttu-id="e515c-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="e515c-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="e515c-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="e515c-110">Remarks</span></span>

<span data-ttu-id="e515c-p101">La méthode **Clone** permet de créer plusieurs objets **Recordset** en double. Chaque jeu d'enregistrements peut avoir son propre enregistrement actif. En soi, l'utilisation de **Clone** n'a pas pour effet de modifier les données contenues dans les objets ou dans leur structure sous-jacente. Lorsque vous utilisez la méthode **Clone**, vous pouvez partager des signets entre deux objets **Recordset2** ou plus, car leurs signets sont interchangeables.</span><span class="sxs-lookup"><span data-stu-id="e515c-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each recordset can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset2** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="e515c-p102">Vous pouvez utiliser la méthode **Clone** si vous souhaitez effectuer une opération sur un jeu d'enregistrements qui requiert plusieurs enregistrements actifs. Il s'agit d'une solution plus rapide et plus efficace que celle qui consiste à ouvrir un deuxième jeu d'enregistrements. Lorsque vous créez un jeu d'enregistrements par le biais de la méthode **Clone**, il lui manque initialement un enregistrement actif. Pour rendre un enregistrement actif avant d'utiliser le clone du jeu d'enregistrements, vous devez définir la propriété **[Bookmark](recordset2-bookmark-property-dao.md)** ou utiliser l'une des méthodes **[Move](recordset-movefirst-method-dao.md)**, l'une des méthodes **[Find](recordset2-findfirst-method-dao.md)** ou la méthode **[Seek](recordset2-seek-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e515c-p102">You can use the **Clone** method when you want to perform an operation on a recordset that requires multiple current records. This is faster and more efficient than opening a second recordset. When you create a recordset with the **Clone** method, it initially lacks a current record. To make a record current before you use the recordset clone, you must set the **[Bookmark](recordset2-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset2-findfirst-method-dao.md)** methods, or the **[Seek](recordset2-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="e515c-p103">Le fait d'appliquer la méthode **[Close](connection-close-method-dao.md)** à l'objet d'origine ou à son double n'a aucune incidence sur l'autre objet. Par exemple, si vous appliquez la méthode **Close** au jeu d'enregistrements d'origine, le clone ne se ferme pas.</span><span class="sxs-lookup"><span data-stu-id="e515c-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original recordset doesn't close the clone.</span></span>

> [!NOTE]
> - <span data-ttu-id="e515c-121">Le fait de fermer un jeu d'enregistrements clone pendant une transaction en attente entraîne une opération **Rollback** implicite.</span><span class="sxs-lookup"><span data-stu-id="e515c-121">Closing a clone recordset within a pending transaction will cause an implicit **Rollback** operation.</span></span>
> - <span data-ttu-id="e515c-p104">Lorsque vous clonez un objet **Recordset** de type table dans un espace de travail Microsoft Access, la définition de la propriété **[Index](recordset2-index-property-dao.md)** n'est pas clonée dans la nouvelle copie du jeu d'enregistrements. Vous devez copier la définition de la propriété **Index** manuellement.</span><span class="sxs-lookup"><span data-stu-id="e515c-p104">When you clone a table-type **Recordset** object in a Microsoft Access workspace, the **[Index](recordset2-index-property-dao.md)** property setting is not cloned on the new copy of the recordset. You must copy the **Index** property setting manually.</span></span>

## <a name="example"></a><span data-ttu-id="e515c-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="e515c-124">Example</span></span>

<span data-ttu-id="e515c-125">Cet exemple de code montre comment utiliser la méthode **Clone** pour créer des copies d'un jeu d'enregistrements tout en laissant le soin à l'utilisateur de positionner le pointeur d'enregistrement de chaque copie indépendamment.</span><span class="sxs-lookup"><span data-stu-id="e515c-125">This example uses the **Clone** method to create copies of a recordset and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```
