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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716249"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="77178-102">UNION, opération (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="77178-102">UNION operation (Microsoft Access SQL)</span></span>

<span data-ttu-id="77178-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77178-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77178-104">Crée une requête Union qui combine les résultats de deux requêtes ou tables indépendantes ou plus.</span><span class="sxs-lookup"><span data-stu-id="77178-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="77178-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77178-105">Syntax</span></span>

<span data-ttu-id="77178-106">\[TABLE\] *Requête1* UNION \[tous les\] \[TABLE\] *requête2* \[UNION \[tous les\] \[TABLE\] *requêten* \[ ...</span><span class="sxs-lookup"><span data-stu-id="77178-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="77178-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="77178-107"></span></span>

<span data-ttu-id="77178-108">L'opération UNION est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="77178-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77178-109">Argument</span><span class="sxs-lookup"><span data-stu-id="77178-109">Part</span></span></p></th>
<th><p><span data-ttu-id="77178-110">Description</span><span class="sxs-lookup"><span data-stu-id="77178-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77178-111"><em>requête1-n</em></span><span class="sxs-lookup"><span data-stu-id="77178-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="77178-112">Instruction SELECT, nom d'une requête enregistrée ou d'une table enregistrée, précédé du mot clé TABLE.</span><span class="sxs-lookup"><span data-stu-id="77178-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="77178-113">Notes</span><span class="sxs-lookup"><span data-stu-id="77178-113">Remarks</span></span>

<span data-ttu-id="77178-p102">Vous pouvez fusionner les résultats de deux ou plusieurs requêtes, tables ou instructions SELECT, dans n'importe quel ordre, en une unique opération UNION. L'exemple suivant fusionne une table existante New Accounts avec une instruction SELECT :</span><span class="sxs-lookup"><span data-stu-id="77178-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="77178-p103">Par défaut, l'opération UNION ne renvoie aucun enregistrement en double mais vous pouvez ajouter le prédicat [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) pour obtenir de façon certaine que tous les enregistrements soient renvoyés. La requête s'exécutera plus rapidement par ailleurs.</span><span class="sxs-lookup"><span data-stu-id="77178-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="77178-118">Toutes les requêtes impliquées dans une opération UNION doivent interroger le même nombre de champs qui, cependant, peuvent avoir des tailles et des types de données différents</span><span class="sxs-lookup"><span data-stu-id="77178-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="77178-p104">N'utilisez des alias que dans la première instruction SELECT ; ils seront ignorés dans toutes les autres. Dans la clause ORDER BY, faites référence aux champs par leurs noms tels qu'ils sont spécifiés dans la première instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="77178-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>

> [!NOTE]
> - <span data-ttu-id="77178-121">Vous pouvez utiliser une clause [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) ou [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) dans chaque argument *requête* pour regrouper les données renvoyées.</span><span class="sxs-lookup"><span data-stu-id="77178-121">You can use a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause in each *query* argument to group the returned data.</span></span>
> - <span data-ttu-id="77178-122">Vous pouvez utiliser une clause [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) à la fin du dernier argument *requête* pour afficher les données renvoyées selon un ordre déterminé.</span><span class="sxs-lookup"><span data-stu-id="77178-122">You can use an [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) clause at the end of the last *query* argument to display the returned data in a specified order.</span></span>

## <a name="example"></a><span data-ttu-id="77178-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="77178-123">Example</span></span>

<span data-ttu-id="77178-124">Dans cet exemple, le nom et la ville de tous les fournisseurs et clients du Brésil sont extraits.</span><span class="sxs-lookup"><span data-stu-id="77178-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="77178-125">Il appelle la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="77178-125">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
