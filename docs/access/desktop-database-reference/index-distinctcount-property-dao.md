---
title: Index.DistinctCount, propriété (DAO)
TOCTitle: DistinctCount Property
ms:assetid: 24cb7247-76b4-1fce-c3c4-892f16634eff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191836(v=office.15)
ms:contentKeyID: 48543767
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053119
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 50a649478a117e79e3cf931976f2520a107ac38d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606624"
---
# <a name="indexdistinctcount-property-dao"></a>Index.DistinctCount, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Renvoie une valeur indiquant le nombre de valeurs uniques pour l'objet **[Index](index-object-dao.md)** inclus dans la table associée (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* DistinctCount

*expression* Variable qui représente un objet **Index.**

## <a name="remarks"></a>Remarques

Vérifiez la propriété **DistinctCount** pour déterminer le nombre de valeurs uniques, ou clés, d'un index. Chaque clé est comptée une seule fois, même si plusieurs occurrences de cette valeur peuvent exister si l'index autorise les doublons. Cette information est utile dans les applications qui tentent d'optimiser l'accès aux données en évaluant les informations d'index. Le nombre de valeurs uniques est également appelé la cardinalité d'un objet **Index**.

La propriété **DistinctCount** ne reflète pas toujours le nombre réel de clés à un moment donné. Par exemple, une modification entraînée par l'annulation d'une transaction ne sera pas immédiatement reflétée dans la propriété **DistinctCount**. La valeur de la propriété **DistinctCount** peut également ne pas refléter la suppression des enregistrements à clés uniques. Le nombre correspond à la réalité immédiatement après utilisation de la méthode **[CreateIndex](tabledef-createindex-method-dao.md)**.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **DistinctCount** pour illustrer la manière de déterminer le nombre de valeurs uniques d'un objet **Index**. Toutefois, cette valeur est correcte uniquement après la création de l'objet **Index**. Elle reste correcte tant que les clés ne sont pas modifiées ou tant qu'aucune nouvelle clé n'est ajoutée et qu'aucune vieille clé n'est supprimée ; sinon, elle n'est pas fiable. (Si vous exécutez cette procédure plusieurs fois, vous pouvez en voir les effets sur les valeurs de la propriété **DistinctCount** des objets Index existants.)

```vb
    Sub DistinctCountX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create and append new Index object to the Employees 
     ' table. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     idxCountry.Fields.Append _ 
     idxCountry.CreateField("Country") 
     .Indexes.Append idxCountry 
     
     ' The collection must be refreshed for the new 
     ' DistinctCount data to be available. 
     .Indexes.Refresh 
     
     ' Enumerate Indexes collection to show the current 
     ' DistinctCount values. 
     Debug.Print "Indexes before adding new record" 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Add a new record to the Employees table. 
     With rstEmployees 
     .AddNew 
     !FirstName = "April" 
     !LastName = "LaMonte" 
     !Country = "Canada" 
     .Update 
     End With 
     
     ' Enumerate Indexes collection to show the modified 
     ' DistinctCount values. 
     Debug.Print "Indexes after adding new record and " & _ 
     "refreshing Indexes" 
     .Indexes.Refresh 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     ' Delete new record because this is a demonstration. 
     With rstEmployees 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Indexes because this is a demonstration. 
     .Indexes.Delete idxCountry.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
