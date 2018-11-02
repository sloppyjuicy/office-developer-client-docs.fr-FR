---
title: Clause PROCEDURE (Microsoft Access SQL)
TOCTitle: PROCEDURE clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dd99fb241572f2e16eae914ba7d1dea31e1d097f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924259"
---
# <a name="procedure-clause-microsoft-access-sql"></a><span data-ttu-id="dc35f-102">Clause PROCEDURE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="dc35f-102">PROCEDURE clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="dc35f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc35f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc35f-104">Définit un nom et des paramètres facultatifs pour une requête.</span><span class="sxs-lookup"><span data-stu-id="dc35f-104">Defines a name and optional parameters for a query.</span></span>

> [!NOTE]
> <span data-ttu-id="dc35f-p101">[!REMARQUE] La clause PROCEDURE a été remplacée par l'instruction PROCEDURE. Bien que la clause PROCEDURE demeure prise en charge, l'instruction PROCEDURE étend les possibilités de la clause PROCEDURE et constitue la syntaxe recommandée.</span><span class="sxs-lookup"><span data-stu-id="dc35f-p101">The PROCEDURE clause has been superseded by the PROCEDURE statement. Although the PROCEDURE clause is still supported, the PROCEDURE statement provides a superset of the capability of the PROCEDURE clause and is the recommended syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc35f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc35f-107">Syntax</span></span>

<span data-ttu-id="dc35f-108">*Nom* de la procédure \[ *param1 type de données*\[, *param2 type de données*\[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="dc35f-108">PROCEDURE *name* \[*param1 datatype*\[, *param2 datatype*\[, …\]\]</span></span>

<span data-ttu-id="dc35f-109">La clause PROCEDURE est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dc35f-109">The PROCEDURE clause has these parts:</span></span>

|<span data-ttu-id="dc35f-110">Argument</span><span class="sxs-lookup"><span data-stu-id="dc35f-110">Part</span></span> |<span data-ttu-id="dc35f-111">Description</span><span class="sxs-lookup"><span data-stu-id="dc35f-111">Description</span></span> |
|:----|:-----------|
|<span data-ttu-id="dc35f-112">*name*</span><span class="sxs-lookup"><span data-stu-id="dc35f-112">*name*</span></span> |<span data-ttu-id="dc35f-p102">Nom donné à la procédure. Ce nom doit respecter les conventions d'affectation des noms standard.</span><span class="sxs-lookup"><span data-stu-id="dc35f-p102">A name for the procedure. It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="dc35f-115">*param1*, *param2*</span><span class="sxs-lookup"><span data-stu-id="dc35f-115">*param1*, *param2*</span></span> |<span data-ttu-id="dc35f-p103">Un ou plusieurs noms de champ ou paramètres. Par exemple :
</span><span class="sxs-lookup"><span data-stu-id="dc35f-p103">One or more field names or parameters. For example:</span></span><br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="dc35f-118">Pour plus d’informations sur les paramètres, voir [paramètres](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="dc35f-118">For more information about parameters, see [parameters](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="dc35f-119">*typedonnées*</span><span class="sxs-lookup"><span data-stu-id="dc35f-119">*datatype*</span></span> | <span data-ttu-id="dc35f-120">Un des principaux [types de données Microsoft Access SQL](sql-data-types.md) ou un de leurs synonymes.</span><span class="sxs-lookup"><span data-stu-id="dc35f-120">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span> |


## <a name="remarks"></a><span data-ttu-id="dc35f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="dc35f-121">Remarks</span></span>

<span data-ttu-id="dc35f-122">Une procédure SQL se compose d'une clause PROCEDURE (qui spécifie le nom de la procédure), d'une liste facultative de définitions de paramètres et d'une seule instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="dc35f-122">An SQL procedure consists of a PROCEDURE clause (which specifies the name of the procedure), an optional list of parameter definitions, and a single SQL statement.</span></span> <span data-ttu-id="dc35f-123">Par exemple, la procédure Get\_composant\_nombre peut s’exécuter une requête qui Récupère un nombre spécifié de composant.</span><span class="sxs-lookup"><span data-stu-id="dc35f-123">For example, the procedure Get\_Part\_Number might run a query that retrieves a specified part number.</span></span>

> [!NOTE]
> - <span data-ttu-id="dc35f-124">Si la clause comporte plusieurs définitions de champ (autrement dit, des paires *param-typedonnées* ), séparez-les par des virgules.</span><span class="sxs-lookup"><span data-stu-id="dc35f-124">If the clause includes more than one field definition (that is, *param-datatype* pairs), separate them with commas.</span></span>
> - <span data-ttu-id="dc35f-125">La clause PROCEDURE doit être suivie d'une instruction SQL (par exemple une instruction [SELECT](select-statement-microsoft-access-sql.md) ou [UPDATE](update-statement-microsoft-access-sql.md)).</span><span class="sxs-lookup"><span data-stu-id="dc35f-125">The PROCEDURE clause must be followed by an SQL statement (for example, a [SELECT](select-statement-microsoft-access-sql.md) or [UPDATE](update-statement-microsoft-access-sql.md) statement).</span></span>

## <a name="example"></a><span data-ttu-id="dc35f-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="dc35f-126">Example</span></span>

<span data-ttu-id="dc35f-127">Cet exemple, la requête categoryList est nommée et la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="dc35f-127">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
