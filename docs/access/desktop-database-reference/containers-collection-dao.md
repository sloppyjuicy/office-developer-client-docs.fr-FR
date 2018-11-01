---
title: Containers Collection (DAO)
TOCTitle: Containers Object
ms:assetid: 4996ee39-ea13-f560-3069-dd7bc6022119
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193464(v=office.15)
ms:contentKeyID: 48544642
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 728d7f22e1da744d70a3c16025530c7cf81dcd84
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889069"
---
# <a name="containers-collection-dao"></a><span data-ttu-id="8ce4f-102">Containers Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="8ce4f-102">Containers Collection (DAO)</span></span>

<span data-ttu-id="8ce4f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ce4f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ce4f-104">Une collection **Containers** contient tous les objets **Container** définis dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="8ce4f-104">A **Containers** collection contains all of the **Container** objects that are defined in a database.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ce4f-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ce4f-105">Remarks</span></span>

<span data-ttu-id="8ce4f-106">Chaque objet de **base de données** possède une collection **Containers** composée d’objets **Container** intégrés.</span><span class="sxs-lookup"><span data-stu-id="8ce4f-106">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects.</span></span> <span data-ttu-id="8ce4f-107">Certains de ces objets **Container** sont définis par le moteur de base de données Microsoft Access alors que les autres peuvent définis par d'autres applications.</span><span class="sxs-lookup"><span data-stu-id="8ce4f-107">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications.</span></span>

## <a name="example"></a><span data-ttu-id="8ce4f-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="8ce4f-108">Example</span></span>

<span data-ttu-id="8ce4f-109">Cet exemple énumère la collection **Containers** de la base de données Northwind et la collection **Properties** de chaque objet **Container** dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8ce4f-109">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

```vb
    Sub ContainerObjectX()
    
       Dim dbsNorthwind As Database
       Dim ctrLoop As Container
       Dim prpLoop As Property
    
       Set dbsNorthwind = OpenDatabase("Northwind.mdb")
    
       With dbsNorthwind
    
          ' Enumerate Containers collection.
          For Each ctrLoop In .Containers
             Debug.Print "Properties of " & ctrLoop.Name _
                & " container"
    
             ' Enumerate Properties collection of each
             ' Container object.
             For Each prpLoop In ctrLoop.Properties
                Debug.Print "  " & prpLoop.Name _
                   & " = " prpLoop
             Next prpLoop
    
          Next ctrLoop
    
          .Close
       End With
    
    End Sub
```
