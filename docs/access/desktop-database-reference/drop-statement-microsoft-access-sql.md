---
title: DROP, instruction (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f31067c96c19804352ca74957e064f9338b49260
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293650"
---
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="7a5d2-102">DROP, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="7a5d2-102">DROP Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="7a5d2-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a5d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a5d2-104">Supprime une table, une procédure ou un affichage existants d’une base de données, ou supprime un index existant d’une table.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="7a5d2-p101">Le moteur de base de données Microsoft Access ne prend pas en charge l'instruction DROP, ni les instructions DDL, avec des bases de données autres que Microsoft Access. Pour cela, utilisez la méthode DAO **Delete**.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-p101">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a5d2-107">Syntax</span></span>

<span data-ttu-id="7a5d2-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span><span class="sxs-lookup"><span data-stu-id="7a5d2-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="7a5d2-109">L’instruction DROP est composée des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7a5d2-109">The DROP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a5d2-110">Quitter</span><span class="sxs-lookup"><span data-stu-id="7a5d2-110">Part</span></span></p></th>
<th><p><span data-ttu-id="7a5d2-111">Description</span><span class="sxs-lookup"><span data-stu-id="7a5d2-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a5d2-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="7a5d2-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="7a5d2-113">Nom de la table à supprimer, ou de la table à partir de laquelle un index doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5d2-114"><em>procedure</em></span><span class="sxs-lookup"><span data-stu-id="7a5d2-114"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="7a5d2-115">Nom de la procédure à supprimer.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a5d2-116"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="7a5d2-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="7a5d2-117">Nom de l’affichage à supprimer.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-117">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5d2-118"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="7a5d2-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="7a5d2-119">Nom de l’index à supprimer de la <em>table.</em></span><span class="sxs-lookup"><span data-stu-id="7a5d2-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7a5d2-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="7a5d2-120">Remarks</span></span>

<span data-ttu-id="7a5d2-121">Vous devez fermer la table avant de pouvoir la supprimer ou de pouvoir y supprimer un index.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="7a5d2-122">Vous pouvez également utiliser [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) pour supprimer un index d'une table.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="7a5d2-p102">Vous pouvez utiliser [CREATE TABLE](create-table-statement-microsoft-access-sql.md) pour créer une table et [CREATE INDEX](create-index-statement-microsoft-access-sql.md) ou ALTER TABLE pour créer un index. Pour modifier une table, utilisez ALTER TABLE.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-p102">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index. To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="7a5d2-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="7a5d2-125">Example</span></span>

<span data-ttu-id="7a5d2-126">Dans l'exemple suivant, un index NewIndex hypothétique est censé exister dans la table Employees de la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="7a5d2-127">Dans cet exemple, l'index NewIndex est supprimé de la table Employees.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-127">This example deletes the index MyIndex from the Employees table.</span></span>

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="7a5d2-128">Dans cet exemple, la table Employees est supprimée de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7a5d2-128">This example deletes the Employees table from the database.</span></span>

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
