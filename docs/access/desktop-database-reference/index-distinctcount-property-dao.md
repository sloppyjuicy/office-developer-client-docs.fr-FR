---
title: Propriété Index.DistinctCount (DAO)
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
ms.openlocfilehash: 62c8681baebf0c1959fcb86df91d61387070adc8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923643"
---
# <a name="indexdistinctcount-property-dao"></a><span data-ttu-id="bbfff-102">Propriété Index.DistinctCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="bbfff-102">Index.DistinctCount property (DAO)</span></span>

<span data-ttu-id="bbfff-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbfff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbfff-104">Renvoie une valeur indiquant le nombre de valeurs uniques pour l'objet **[Index](index-object-dao.md)** inclus dans la table associée (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="bbfff-104">Returns a value that indicates the number of unique values for the **[Index](index-object-dao.md)** object that are included in the associated table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="bbfff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbfff-105">Syntax</span></span>

<span data-ttu-id="bbfff-106">*expression* . DistinctCount</span><span class="sxs-lookup"><span data-stu-id="bbfff-106">*expression* .DistinctCount</span></span>

<span data-ttu-id="bbfff-107">*expression* Variable qui représente un objet **Index** .</span><span class="sxs-lookup"><span data-stu-id="bbfff-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbfff-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="bbfff-108">Remarks</span></span>

<span data-ttu-id="bbfff-p101">Vérifiez la propriété **DistinctCount** pour déterminer le nombre de valeurs uniques, ou clés, d'un index. Chaque clé est comptée une seule fois, même si plusieurs occurrences de cette valeur peuvent exister si l'index autorise les doublons. Cette information est utile dans les applications qui tentent d'optimiser l'accès aux données en évaluant les informations d'index. Le nombre de valeurs uniques est également appelé la cardinalité d'un objet **Index**.</span><span class="sxs-lookup"><span data-stu-id="bbfff-p101">Check the **DistinctCount** property to determine the number of unique values, or keys, in an index. Any key is counted only once, even though there may be multiple occurrences of that value if the index permits duplicate values. This information is useful in applications that attempt to optimize data access by evaluating index information. The number of unique values is also known as the cardinality of an **Index** object.</span></span>

<span data-ttu-id="bbfff-p102">La propriété **DistinctCount** ne reflète pas toujours le nombre réel de clés à un moment donné. Par exemple, une modification entraînée par l'annulation d'une transaction ne sera pas immédiatement reflétée dans la propriété **DistinctCount**. La valeur de la propriété **DistinctCount** peut également ne pas refléter la suppression des enregistrements à clés uniques. Le nombre correspond à la réalité immédiatement après utilisation de la méthode **[CreateIndex](tabledef-createindex-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="bbfff-p102">The **DistinctCount** property won't always reflect the actual number of keys at a particular time. For example, a change caused by a rolled back transaction won't be reflected immediately in the **DistinctCount** property. The **DistinctCount** property value also may not reflect the deletion of records with unique keys. The number will be accurate immediately after you use the **[CreateIndex](tabledef-createindex-method-dao.md)** method.</span></span>

## <a name="example"></a><span data-ttu-id="bbfff-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="bbfff-117">Example</span></span>

<span data-ttu-id="bbfff-p103">Cet exemple utilise la propriété **DistinctCount** pour illustrer la manière de déterminer le nombre de valeurs uniques d'un objet **Index**. Toutefois, cette valeur est correcte uniquement après la création de l'objet **Index**. Elle reste correcte tant que les clés ne sont pas modifiées ou tant qu'aucune nouvelle clé n'est ajoutée et qu'aucune vieille clé n'est supprimée ; sinon, elle n'est pas fiable. (Si vous exécutez cette procédure plusieurs fois, vous pouvez en voir les effets sur les valeurs de la propriété **DistinctCount** des objets Index existants.)</span><span class="sxs-lookup"><span data-stu-id="bbfff-p103">This example uses the **DistinctCount** property to show how you can determine the number of unique values in an **Index** object. However, this value is only accurate immediately after creating the **Index**. It will remain accurate if no keys change, or if new keys are added and no old keys are deleted; otherwise, it will not be reliable. (If this procedure is run several times, you can see the effect on the **DistinctCount** property values of the existing Index objects.)</span></span>

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
