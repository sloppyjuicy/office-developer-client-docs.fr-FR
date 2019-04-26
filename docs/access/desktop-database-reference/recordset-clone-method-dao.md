---
title: Recordset.Clone, méthode (DAO)
TOCTitle: Clone Method
ms:assetid: 50cbc011-7e72-4dee-488d-96e681618e8e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193824(v=office.15)
ms:contentKeyID: 48544802
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052909
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: ecc5592893c1caee16f0a00687ce50f68b05e9c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300657"
---
# <a name="recordsetclone-method-dao"></a><span data-ttu-id="d2e07-102">Recordset.Clone, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="d2e07-102">Recordset.Clone Method (DAO)</span></span>

<span data-ttu-id="d2e07-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2e07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2e07-104">Crée un doublon d’objet**[Recordset](recordset-object-dao.md)** qui fait référence à la cellule d’origine de l’objet**Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d2e07-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2e07-105">Syntax</span></span>

<span data-ttu-id="d2e07-106">*expression* . Clone</span><span class="sxs-lookup"><span data-stu-id="d2e07-106">expression  . Clone</span></span>

<span data-ttu-id="d2e07-107">*expression* Variable représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d2e07-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2e07-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2e07-108">Return value</span></span>

<span data-ttu-id="d2e07-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="d2e07-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="d2e07-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2e07-110">Remarks</span></span>

<span data-ttu-id="d2e07-p101">Utilisez la méthode **Clone** pour créer plusieurs objets **Recordset** dupliqués. Chaque objet **Recordset** peut avoir son propre enregistrement actif. L'utilisation de la seule méthode **Clone** ne modifie pas les données dans les objets ou leurs structures sous-jacentes. Lorsque vous utilisez la méthode **Clone**, vous pouvez partager des signets entre deux ou plusieurs objets **Recordset** dans la mesure où leurs signets sont interchangeables.</span><span class="sxs-lookup"><span data-stu-id="d2e07-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each **Recordset** can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="d2e07-p102">Vous pouvez avoir recours à la méthode **Clone** lorsque vous souhaitez effectuer une opération sur un objet **Recordset** qui exige plusieurs enregistrements actifs dans la mesure où elle est plus rapide et efficace que l'ouverture d'un deuxième objet **Recordset**. Lorsque vous créez un objet **Recordset** avec la méthode **Clone**, il ne possède pas au départ d'enregistrement actif. Pour disposer d'un enregistrement actif avant d'utiliser le clone de l'objet **Recordset**, vous devez définir la propriété **[Bookmark](recordset-bookmark-property-dao.md)** ou utiliser l'une des méthodes **[Move](recordset-movefirst-method-dao.md)**, l'une des méthodes **[Find](recordset-findfirst-method-dao.md)** ou la méthode **[Seek](recordset-seek-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="d2e07-p102">You can use the **Clone** method when you want to perform an operation on a **Recordset** that requires multiple current records. This is faster and more efficient than opening a second **Recordset**. When you create a **Recordset** with the **Clone** method, it initially lacks a current record. To make a record current before you use the **Recordset** clone, you must set the **[Bookmark](recordset-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset-findfirst-method-dao.md)** methods, or the **[Seek](recordset-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="d2e07-p103">L'emploi de la méthode **[Close](connection-close-method-dao.md)** sur l'objet original ou dupliqué n'a aucune incidence sur l'autre objet. Ainsi, l'appel de la méthode **Close** sur l'objet **Recordset** d'origine ne ferme pas le clone.</span><span class="sxs-lookup"><span data-stu-id="d2e07-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original **Recordset** doesn't close the clone.</span></span>

> [!NOTE]
> - <span data-ttu-id="d2e07-121">Le fait de fermer un jeu d'enregistrements clone pendant une transaction en attente entraîne une opération **Rollback** implicite.</span><span class="sxs-lookup"><span data-stu-id="d2e07-121">Closing a clone recordset within a pending transaction will cause an implicit **Rollback** operation.</span></span>
> - <span data-ttu-id="d2e07-p104">Lorsque vous clonez un objet **Recordset** de type table dans un espace de travail Microsoft Access, la définition de la propriété **[Index](recordset2-index-property-dao.md)** n'est pas clonée dans la nouvelle copie du jeu d'enregistrements. Vous devez copier la définition de la propriété **Index** manuellement.</span><span class="sxs-lookup"><span data-stu-id="d2e07-p104">When you clone a table-type **Recordset** object in a Microsoft Access workspace, the **[Index](recordset2-index-property-dao.md)** property setting is not cloned on the new copy of the recordset. You must copy the **Index** property setting manually.</span></span>

## <a name="example"></a><span data-ttu-id="d2e07-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="d2e07-124">Example</span></span>

<span data-ttu-id="d2e07-125">Cet exemple utilise la méthode **Clone** pour créer des copies d'un objet **Recordset** puis permet à l'utilisateur de positionner le pointeur d'enregistrement de chaque copie indépendamment des autres.</span><span class="sxs-lookup"><span data-stu-id="d2e07-125">This example uses the **Clone** method to create copies of a **Recordset** and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset 
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
