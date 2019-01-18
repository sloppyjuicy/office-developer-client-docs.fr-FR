---
title: Instruction EXECUTE (Microsoft Access SQL)
TOCTitle: EXECUTE statement (Microsoft Access SQL)
ms:assetid: 9ec4d9ee-db2a-0319-3ccf-c035d67a1496
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198330(v=office.15)
ms:contentKeyID: 48546667
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277471
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: df70d2728732f33161622ce71fc9273bd9f016f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701941"
---
# <a name="execute-statement-microsoft-access-sql"></a><span data-ttu-id="c9867-102">Instruction EXECUTE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c9867-102">EXECUTE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="c9867-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9867-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9867-104">Utilisée pour invoquer l'exécution d'une procédure.</span><span class="sxs-lookup"><span data-stu-id="c9867-104">Used to invoke the execution of a procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9867-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9867-105">Syntax</span></span>

<span data-ttu-id="c9867-106">EXECUTE *procédure* \[ *param1*\[, *param2*\[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="c9867-106">EXECUTE *procedure* \[*param1*\[, *param2*\[, …\]\]</span></span>

<span data-ttu-id="c9867-107">L'instruction EXECUTE est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c9867-107">The EXECUTE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9867-108">Argument</span><span class="sxs-lookup"><span data-stu-id="c9867-108">Part</span></span></p></th>
<th><p><span data-ttu-id="c9867-109">Description</span><span class="sxs-lookup"><span data-stu-id="c9867-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9867-110"><em>procédure</em></span><span class="sxs-lookup"><span data-stu-id="c9867-110"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="c9867-111">Nom de la procédure à exécuter.</span><span class="sxs-lookup"><span data-stu-id="c9867-111">The name of the procedure that is to be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9867-112"><em>param1, param2, …</em></span><span class="sxs-lookup"><span data-stu-id="c9867-112"><em>param1, param2, …</em></span></span></p></td>
<td><p><span data-ttu-id="c9867-113">Valeurs des paramètres définis par la procédure.</span><span class="sxs-lookup"><span data-stu-id="c9867-113">Values for the parameters defined by the procedure.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="c9867-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="c9867-114">Example</span></span>

<span data-ttu-id="c9867-115">Cet exemple, la requête categoryList est nommée et la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="c9867-115">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        Execute EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
