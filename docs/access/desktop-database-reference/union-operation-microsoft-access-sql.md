---
title: UNION, opération (Microsoft Access SQL)
TOCTitle: UNION Operation (Microsoft Access SQL)
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
ms.openlocfilehash: 63ff883f35dabbbd69e1bf144eb32016f303c7ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879108"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="e78d3-102">UNION, opération (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e78d3-102">UNION Operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="e78d3-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e78d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e78d3-104">Crée une requête Union qui combine les résultats de deux requêtes ou tables indépendantes ou plus.</span><span class="sxs-lookup"><span data-stu-id="e78d3-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e78d3-105">Syntax</span></span>

<span data-ttu-id="e78d3-106">\[TABLE\] *Requête1* UNION \[tous les\] \[TABLE\] *requête2* \[UNION \[tous les\] \[TABLE\] *requêten* \[ ...</span><span class="sxs-lookup"><span data-stu-id="e78d3-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="e78d3-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="e78d3-107"></span></span>

<span data-ttu-id="e78d3-108">L'opération UNION est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e78d3-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e78d3-109">Argument</span><span class="sxs-lookup"><span data-stu-id="e78d3-109">Part</span></span></p></th>
<th><p><span data-ttu-id="e78d3-110">Description</span><span class="sxs-lookup"><span data-stu-id="e78d3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e78d3-111"><em>requête1-n</em></span><span class="sxs-lookup"><span data-stu-id="e78d3-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="e78d3-112">Instruction SELECT, nom d'une requête enregistrée ou d'une table enregistrée, précédé du mot clé TABLE.</span><span class="sxs-lookup"><span data-stu-id="e78d3-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e78d3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e78d3-113">Remarks</span></span>

<span data-ttu-id="e78d3-p102">Vous pouvez fusionner les résultats de deux ou plusieurs requêtes, tables ou instructions SELECT, dans n'importe quel ordre, en une unique opération UNION. L'exemple suivant fusionne une table existante New Accounts avec une instruction SELECT :</span><span class="sxs-lookup"><span data-stu-id="e78d3-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="e78d3-p103">Par défaut, l'opération UNION ne renvoie aucun enregistrement en double mais vous pouvez ajouter le prédicat [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) pour obtenir de façon certaine que tous les enregistrements soient renvoyés. La requête s'exécutera plus rapidement par ailleurs.</span><span class="sxs-lookup"><span data-stu-id="e78d3-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="e78d3-118">Toutes les requêtes impliquées dans une opération UNION doivent interroger le même nombre de champs qui, cependant, peuvent avoir des tailles et des types de données différents</span><span class="sxs-lookup"><span data-stu-id="e78d3-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="e78d3-p104">N'utilisez des alias que dans la première instruction SELECT ; ils seront ignorés dans toutes les autres. Dans la clause ORDER BY, faites référence aux champs par leurs noms tels qu'ils sont spécifiés dans la première instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="e78d3-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="e78d3-121">Vous pouvez utiliser une clause <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> ou <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> dans chaque argument <EM>requête</EM> pour regrouper les données renvoyées.</span><span class="sxs-lookup"><span data-stu-id="e78d3-121">You can use a <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> or <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> clause in each <EM>query</EM> argument to group the returned data.</span></span></P>
> <LI>
> <P><span data-ttu-id="e78d3-122">Vous pouvez utiliser une clause <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> à la fin du dernier argument <EM>requête</EM> pour afficher les données renvoyées selon un ordre déterminé.</span><span class="sxs-lookup"><span data-stu-id="e78d3-122">You can use an <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> clause at the end of the last <EM>query</EM> argument to display the returned data in a specified order.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="e78d3-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="e78d3-123">Example</span></span>

<span data-ttu-id="e78d3-124">Dans cet exemple, le nom et la ville de tous les fournisseurs et clients du Brésil sont extraits.</span><span class="sxs-lookup"><span data-stu-id="e78d3-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span>

<span data-ttu-id="e78d3-125">La procédure EnumFields (que vous pouvez trouver dans l'exemple d'instruction SELECT) est appelée dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="e78d3-125">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
