---
title: UPDATE, instruction (Microsoft Access SQL)
TOCTitle: UPDATE statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 6a0404c21b308f6e389ee5577cc212763e660774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306243"
---
# <a name="update-statement-microsoft-access-sql"></a><span data-ttu-id="3147b-102">UPDATE, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="3147b-102">UPDATE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="3147b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3147b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3147b-104">Crée une  qui modifie les valeurs des champs d’une table spécifiée en fonction de critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3147b-104">Creates an update query that changes values in fields in a specified table based on specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="3147b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3147b-105">Syntax</span></span>

<span data-ttu-id="3147b-106">UPDATE *table* SET *newvalue* WHERE *criteria*;</span><span class="sxs-lookup"><span data-stu-id="3147b-106">UPDATE *table* 
    SET *newvalue* 
    WHERE *criteria*;</span></span>

<span data-ttu-id="3147b-107">L’instruction SELECT comprend les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="3147b-107">The UPDATE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3147b-108">Quitter</span><span class="sxs-lookup"><span data-stu-id="3147b-108">Part</span></span></p></th>
<th><p><span data-ttu-id="3147b-109">Description</span><span class="sxs-lookup"><span data-stu-id="3147b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3147b-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="3147b-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="3147b-111">Nom de la table contenant les données que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="3147b-111">The name of the table containing the data you want to modify.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3147b-112"><em>newvalue</em></span><span class="sxs-lookup"><span data-stu-id="3147b-112"><em>newvalue</em></span></span></p></td>
<td><p><span data-ttu-id="3147b-113">Expression qui détermine la valeur à insérer dans un champ particulier dans les enregistrements mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3147b-113">An expression that determines the value to be inserted into a particular field in the updated records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3147b-114"><em>critères</em></span><span class="sxs-lookup"><span data-stu-id="3147b-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="3147b-p101">Expression qui détermine quels enregistrements sont mis à jour. Seuls les enregistrements correspondant à l’expression sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3147b-p101">An expression that determines which records will be updated. Only records that satisfy the expression are updated.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3147b-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="3147b-117">Remarks</span></span>

<span data-ttu-id="3147b-118">L’instruction UPDATE est particulièrement utile lorsque vous souhaitez modifier de nombreux enregistrements ou que les enregistrements que vous souhaitez modifier résident dans plusieurs tables.</span><span class="sxs-lookup"><span data-stu-id="3147b-118">UPDATE is especially useful when you want to change many records or when the records that you want to change are in multiple tables.</span></span>

<span data-ttu-id="3147b-p102">Vous pouvez modifier plusieurs champs simultanément. L’exemple suivant augmente les valeurs de OrderAmount de 10 pour cent et les valeurs de Freight de 3 pour cent pour les transporteurs résidant au Royaume-Uni (UK) :</span><span class="sxs-lookup"><span data-stu-id="3147b-p102">You can change several fields at the same time. The following example increases the Order Amount values by 10 percent and the Freight values by 3 percent for shippers in the United Kingdom:</span></span>

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- <span data-ttu-id="3147b-p103">L’instruction UPDATE ne génère pas de jeu de résultats. Par ailleurs, une fois les enregistrements mis à jour à l’aide d’une requête de mise à jour, vous ne pouvez pas annuler l’opération. Pour savoir quels enregistrements ont été mis à jour, commencez par examiner les résultats d’une  qui utilise les mêmes critères, puis exécutez la requête de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3147b-p103">UPDATE does not generate a result set. Also, after you update records using an update query, you cannot undo the operation. If you want to know which records were updated, first examine the results of a select query that uses the same criteria, and then run the update query.</span></span>
- <span data-ttu-id="3147b-124">Conservez toujours des copies de sauvegarde de vos données.</span><span class="sxs-lookup"><span data-stu-id="3147b-124">Maintain backup copies of your data at all times.</span></span> <span data-ttu-id="3147b-125">Si vous mettez à jour des enregistrements par inadvertance, vous pourrez les récupérer à partir de vos copies de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="3147b-125">If you update the wrong records, you can retrieve them from your backup copies.</span></span>



## <a name="example"></a><span data-ttu-id="3147b-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="3147b-126">Example</span></span>

<span data-ttu-id="3147b-127">Cet exemple modifie les valeurs dans le champ responsable à 5 pour tous les enregistrements d’employé qui ont actuellement valeurs responsable de 2.</span><span class="sxs-lookup"><span data-stu-id="3147b-127">This example changes values in the ReportsTo field to 5 for all employee records that currently have ReportsTo values of 2.</span></span>

```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```
