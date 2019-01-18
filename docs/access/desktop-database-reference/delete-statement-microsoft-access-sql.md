---
title: DELETE, instruction (Microsoft Access SQL)
TOCTitle: DELETE statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: a4ef478e74f9851012d6f749e64b4ddb34f3a959
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715619"
---
# <a name="delete-statement-microsoft-access-sql"></a><span data-ttu-id="8acd5-102">DELETE, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8acd5-102">DELETE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="8acd5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8acd5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8acd5-104">Crée une requête qui supprime les enregistrements d’une ou de plusieurs tables répertoriées dans la clause [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) qui satisfont à la clause [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="8acd5-104">Creates a delete query that removes records from one or more of the tables listed in the [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause that satisfy the [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="8acd5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8acd5-105">Syntax</span></span>

<span data-ttu-id="8acd5-106">SUPPRIMER \[ *table*. \* \] De *table* WHERE *critère*</span><span class="sxs-lookup"><span data-stu-id="8acd5-106">DELETE \[*table*.\*\] FROM *table* WHERE *criteria*</span></span>

<span data-ttu-id="8acd5-107">L'instruction DELETE est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8acd5-107">The DELETE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8acd5-108">Argument</span><span class="sxs-lookup"><span data-stu-id="8acd5-108">Part</span></span></p></th>
<th><p><span data-ttu-id="8acd5-109">Description</span><span class="sxs-lookup"><span data-stu-id="8acd5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8acd5-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="8acd5-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="8acd5-111">Nom facultatif de la table de laquelle des enregistrements sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="8acd5-111">The optional name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8acd5-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="8acd5-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="8acd5-113">Nom de la table de laquelle des enregistrements sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="8acd5-113">The name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8acd5-114"><em>criteria</em></span><span class="sxs-lookup"><span data-stu-id="8acd5-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="8acd5-115">Expression qui détermine les enregistrements à supprimer.</span><span class="sxs-lookup"><span data-stu-id="8acd5-115">An expression that determines which records to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8acd5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8acd5-116">Remarks</span></span>

<span data-ttu-id="8acd5-117">DELETE est particulièrement utile pour supprimer de nombreux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="8acd5-117">DELETE is especially useful when you want to delete many records.</span></span>

<span data-ttu-id="8acd5-p101">Pour supprimer une table entière de la base de données, vous pouvez utiliser la méthode **Execute** avec une instruction [DROP](drop-statement-microsoft-access-sql.md). Si vous supprimez la table, sa structure est perdue. En revanche, si vous utilisez la clause DELETE, seules les données sont supprimées ; la structure de la table et toutes ses propriétés, telles que les attributs des champs et les index, sont conservées.</span><span class="sxs-lookup"><span data-stu-id="8acd5-p101">To drop an entire table from the database, you can use the **Execute** method with a [DROP](drop-statement-microsoft-access-sql.md) statement. If you delete the table, however, the structure is lost. In contrast, when you use DELETE, only the data is deleted; the table structure and all of the table properties, such as field attributes and indexes, remain intact.</span></span>

<span data-ttu-id="8acd5-p102">Vous pouvez utiliser DELETE pour supprimer des enregistrements des tables qui sont dans une relation de un à plusieurs avec d'autres tables. Les opérations de suppression en cascade entraînent la suppression des enregistrements des tables qui sont du côté 'plusieurs' de la relation lorsque l'enregistrement correspondant du côté 'un' est supprimé dans la requête. Par exemple, dans la relation entre les tables Customers et Orders, la table Customers est du côté 'un' et la table Orders est du côté 'plusieurs' de la relation. Lorsqu'un enregistrement est supprimé de la table Customers, les enregistrements correspondants sont supprimés de la table Orders si l'option de suppression en cascade est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8acd5-p102">You can use DELETE to remove records from tables that are in a one-to-many relationship with other tables. Cascade delete operations cause the records in tables that are on the many side of the relationship to be deleted when the corresponding record in the one side of the relationship is deleted in the query. For example, in the relationship between the Customers and Orders tables, the Customers table is on the one side and the Orders table is on the many side of the relationship. Deleting a record from Customers results in the corresponding Orders records being deleted if the cascade delete option is specified.</span></span>

<span data-ttu-id="8acd5-p103">Une requête de suppression supprime les enregistrements, et pas seulement les données dans des champs spécifiques. Si vous voulez supprimer des valeurs dans un champ spécifique, créez une requête de mise à jour qui remplacent ces valeurs par des valeurs **Null**.</span><span class="sxs-lookup"><span data-stu-id="8acd5-p103">A delete query deletes entire records, not just data in specific fields. If you want to delete values in a specific field, create an update query that changes the values to **Null**.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="8acd5-p104">Une fois que des enregistrements sont supprimés à l'aide d'une requête de suppression, il n'est pas possible d'annuler cette opération. Si vous voulez savoir quels enregistrements ont été supprimés, examinez d'abord les résultats d'une requête de sélection qui utilise les mêmes critères, puis exécutez la requête de suppression.</span><span class="sxs-lookup"><span data-stu-id="8acd5-p104">After you remove records using a delete query, you cannot undo the operation. If you want to know which records were deleted, first examine the results of a select query that uses the same criteria, and then run the delete query.</span></span>
> - <span data-ttu-id="8acd5-p105">Conservez toujours des copies de sauvegarde de vos données. Si vous supprimez les mauvais enregistrements, vous pourrez alors les récupérer à partir de vos copies de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="8acd5-p105">Maintain backup copies of your data at all times. If you delete the wrong records, you can retrieve them from your backup copies.</span></span>

## <a name="example"></a><span data-ttu-id="8acd5-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="8acd5-131">Example</span></span>

<span data-ttu-id="8acd5-p106">Dans cet exemple, tous les enregistrements d'employés dont le titre est Trainee, sont supprimés. Lorsque la clause FROM ne comporte qu'une seule table, vous n'avez pas besoin d'indiquer le nom de la table dans l'instruction DELETE.

</span><span class="sxs-lookup"><span data-stu-id="8acd5-p106">This example deletes all records for employees whose title is Trainee. When the FROM clause includes only one table, you do not have to list the table name in the DELETE statement.</span></span>

```vb
    Sub DeleteX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete employee records where title is Trainee.     
        dbs.Execute "DELETE * FROM " _ 
            & "Employees WHERE Title = 'Trainee';" 
         
        dbs.Close 
     
    End Sub
```
