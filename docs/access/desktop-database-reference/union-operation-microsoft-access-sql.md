---
title: UNION, opération (Microsoft Access SQL)
TOCTitle: UNION operation (Microsoft Access SQL)
ms:assetid: a5139921-51e5-7d96-74e3-11c3fd5f7eaa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821131(v=office.15)
ms:contentKeyID: 48546826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277582
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f842e662f2576d8aab5f3857877f45e380d3d3b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314699"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="45470-102">UNION, opération (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="45470-102">UNION Operation (Microsoft Access SQL)</span></span>

<span data-ttu-id="45470-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45470-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45470-104">L’opération UNION dans Access crée une requête Union qui combine les résultats d’au moins deux requêtes ou tables indépendantes.</span><span class="sxs-lookup"><span data-stu-id="45470-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="45470-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45470-105">Syntax</span></span>

<span data-ttu-id="45470-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span><span class="sxs-lookup"><span data-stu-id="45470-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="45470-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="45470-107"></span></span>

<span data-ttu-id="45470-108">L’opération UNION comprend les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="45470-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45470-109">Quitter</span><span class="sxs-lookup"><span data-stu-id="45470-109">Part</span></span></p></th>
<th><p><span data-ttu-id="45470-110">Description</span><span class="sxs-lookup"><span data-stu-id="45470-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45470-111"><em>query1-n</em></span><span class="sxs-lookup"><span data-stu-id="45470-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="45470-112">Instruction SELECT, nom d’une requête stockée, ou nom d’une table stockée précédés du mot clé TABLE.</span><span class="sxs-lookup"><span data-stu-id="45470-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="45470-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="45470-113">Remarks</span></span>

<span data-ttu-id="45470-p102">Vous pouvez fusionner les résultats d’au moins deux requêtes, tables et instructions SELECT, dans n’importe quelle combinaison, en une seule opération UNION. L’exemple suivant fusionne une table existante nommée New Accounts (Nouveaux comptes) et une instruction SELECT :</span><span class="sxs-lookup"><span data-stu-id="45470-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="45470-p103">Par défaut, aucun enregistrement en double n’est renvoyé lorsque vous utilisez une opération UNION. Toutefois, vous pouvez inclure le prédicat ALL pour vous assurer que tous les enregistrements soient renvoyés. Cela accélère également l’exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="45470-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="45470-118">Toutes les requêtes dans une opération UNION doivent demander le même nombre de champs. Toutefois, les champs ne doivent pas nécessairement avoir les même taille ou .</span><span class="sxs-lookup"><span data-stu-id="45470-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="45470-p104">Utiliser des alias uniquement dans la première instruction SELECT, car ils sont ignorés dans les autres. Dans la clause ORDER BY, faites référence aux champs par la manière dont ils sont appelés dans la première instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="45470-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>

> [!NOTE]
> - <span data-ttu-id="45470-121">Vous pouvez utiliser une clause GROUP BY ou HAVING dans chaque argument [requête](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) pour regrouper les données renvoyées.</span><span class="sxs-lookup"><span data-stu-id="45470-121">You can use a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause in each *query* argument to group the returned data.</span></span>
> - <span data-ttu-id="45470-122">Vous pouvez utiliser une clause ORDER BY à la fin du dernier argument [requête](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) pour afficher les données renvoyées dans un ordre spécifié.</span><span class="sxs-lookup"><span data-stu-id="45470-122">You can use an [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) clause at the end of the last *query* argument to display the returned data in a specified order.</span></span>

## <a name="example"></a><span data-ttu-id="45470-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="45470-123">Example</span></span>

<span data-ttu-id="45470-124">Cet exemple extrait les noms et les villes de tous les fournisseurs et clients au Brésil.</span><span class="sxs-lookup"><span data-stu-id="45470-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="45470-125">Il appelle la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="45470-125">This example calls the EnumFields procedure, which you can find in the SELECT statement example.

</span></span>

```vb
    Sub UnionX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Retrieve the names and cities of all suppliers  
        ' and customers in Brazil. 
        Set rst = dbs.OpenRecordset("SELECT CompanyName," _ 
            & " City FROM Suppliers" _ 
            & " WHERE Country = 'Brazil' UNION" _ 
            & " SELECT CompanyName, City FROM Customers" _ 
            & " WHERE Country = 'Brazil';") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub
```
