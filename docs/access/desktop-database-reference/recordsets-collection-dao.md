---
title: Recordsets Collection (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8779a0a7ff8b298c8773d661deb525ab5aa3c04
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471728"
---
# <a name="recordsets-collection-dao"></a><span data-ttu-id="83f21-102">Recordsets Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="83f21-102">Recordsets Collection (DAO)</span></span>

<span data-ttu-id="83f21-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="83f21-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="83f21-104">Une collection **Recordsets** contient tous les objets **Recordset** ouverts, dans un objet **Connection** ou **Database**.</span><span class="sxs-lookup"><span data-stu-id="83f21-104">A **Recordsets** collection contains all open **Recordset** objects in a **Connection** or **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="83f21-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="83f21-105">Remarks</span></span>

<span data-ttu-id="83f21-106">Lorsque vous utilisez des objets DAO, vous manipulez les données presque exclusivement à l'aide des objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="83f21-106">When you use DAO objects, you manipulate data almost entirely using **Recordset** objects.</span></span>

<span data-ttu-id="83f21-107">Un objet **Recordset** est automatiquement ajouté à la collection **Recordsets** lorsque vous ouvrez l'objet **Recordset** et supprimé lorsque vous le fermez.</span><span class="sxs-lookup"><span data-stu-id="83f21-107">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the **Recordset** object, and is automatically removed when you close it.</span></span>

<span data-ttu-id="83f21-p101">Vous pouvez créer autant de variables d'objet **Recordset** que vous le souhaitez. Des objets **Recordset** différents peuvent accéder aux mêmes tables, requêtes et champs sans créer de conflits.</span><span class="sxs-lookup"><span data-stu-id="83f21-p101">You can create as many **Recordset** object variables as needed. Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="83f21-110">Pour faire référence à un objet **Recordset** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="83f21-110">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="83f21-111">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="83f21-111">**Recordsets**(0)</span></span>

- <span data-ttu-id="83f21-112">**Jeux d’enregistrements** (« nom »)</span><span class="sxs-lookup"><span data-stu-id="83f21-112">**Recordsets**("name")</span></span>

- <span data-ttu-id="83f21-113">**Jeux d’enregistrements**\!\[nom\]</span><span class="sxs-lookup"><span data-stu-id="83f21-113">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="83f21-p102">[!REMARQUE] Vous pouvez ouvrir plusieurs fois un objet **Recordset** à partir de la même source de données ou base de données en créant des noms en double dans la collection **Recordsets**. Vous devez attribuer des objets **Recordset** à des variables d'objet et y faire référence par nom de variable.</span><span class="sxs-lookup"><span data-stu-id="83f21-p102">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection. You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="83f21-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="83f21-116">Example</span></span>

<span data-ttu-id="83f21-117">L'exemple ci-dessous illustre les objets **Recordset** et la collection **Recordsets** en ouvrant quatre types d'objet **Recordsets** différents, en énumérant la collection Recordsets de l'objet **Database** actif et en énumérant la collection **Properties** de chaque objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="83f21-117">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
