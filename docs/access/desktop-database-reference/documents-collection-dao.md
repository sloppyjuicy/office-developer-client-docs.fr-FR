---
title: Documents Collection (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ed91166c8a244c20848069ecfd936a25c10accd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878163"
---
# <a name="documents-collection-dao"></a>Documents Collection (DAO)


**S’applique à**: Access 2013, Office 2013

Une collection **Documents** contient tous les objets **Document** d'un type spécifique d'objet (bases de données de moteur de base de données Microsoft Access uniquement).

## <a name="remarks"></a>Remarques

Chaque objet **Container** est doté d'une collection **Documents** contenant les objets **Document** qui décrivent les instances des objets intégrés du type spécifié dans l'objet **Container**.

Pour faire référence à un objet **Document** d'une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des syntaxes suivantes :

  - **Documents**(0)

  - **Documents** («*nom*»)

  - **Documents**\!\[*nom*\]

## <a name="example"></a>Exemple

Cet exemple énumère la collection **Documents** du conteneur Tables, puis la collection **Properties** du premier objet **Document** de la collection.

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

