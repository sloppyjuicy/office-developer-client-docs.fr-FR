---
title: Collection Containers (DAO)
TOCTitle: Containers Object
ms:assetid: 4996ee39-ea13-f560-3069-dd7bc6022119
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193464(v=office.15)
ms:contentKeyID: 48544642
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be25a2f8b5d6da7b569858d758b3fb541cf9be51
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920437"
---
# <a name="containers-collection-dao"></a>Collection Containers (DAO)

**S’applique à**: Access 2013, Office 2013

Une collection **Containers** contient tous les objets **Container** définis dans une base de données.

## <a name="remarks"></a>Remarques

Chaque objet de **base de données** possède une collection **Containers** composée d’objets **Container** intégrés. Certains de ces objets **Container** sont définis par le moteur de base de données Microsoft Access alors que les autres peuvent définis par d'autres applications.

## <a name="example"></a>Exemple

Cet exemple énumère la collection **Containers** de la base de données Northwind et la collection **Properties** de chaque objet **Container** dans la collection.

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
