---
title: CREATE PROCEDURE, instruction (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: f223e164bd36a6a1a76140a28dd57cd2005e4a20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295401"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="99c85-102">CREATE PROCEDURE, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="99c85-102">CREATE PROCEDURE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="99c85-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="99c85-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="99c85-104">Crée une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="99c85-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="99c85-105">Le moteur de base de données Microsoft Access ne prend pas en charge l'instruction CREATE PROCEDURE, ni les instructions DDL, avec des bases de données autres que celles de type Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="99c85-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c85-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99c85-106">Syntax</span></span>

<span data-ttu-id="99c85-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span><span class="sxs-lookup"><span data-stu-id="99c85-107">CREATE PROCEDURE procedure
    [param1 datatype[, param2 datatype[, …]] AS sqlstatement</span></span>

<span data-ttu-id="99c85-108">L’instruction CREATE PROCEDURE comprend les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="99c85-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="99c85-109">Quitter</span><span class="sxs-lookup"><span data-stu-id="99c85-109">Part</span></span>|<span data-ttu-id="99c85-110">Description</span><span class="sxs-lookup"><span data-stu-id="99c85-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="99c85-111">*procedure*</span><span class="sxs-lookup"><span data-stu-id="99c85-111">*procedure*</span></span>|<span data-ttu-id="99c85-112">Nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="99c85-112">A name for the procedure.</span></span> <span data-ttu-id="99c85-113">Ce nom doit respecter les conventions d'affectation des noms standard.</span><span class="sxs-lookup"><span data-stu-id="99c85-113">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="99c85-114">*param1*, *param2*</span><span class="sxs-lookup"><span data-stu-id="99c85-114">*param1*, *param2*</span></span>|<span data-ttu-id="99c85-115">De un à 255 noms de champs ou paramètres.</span><span class="sxs-lookup"><span data-stu-id="99c85-115">From one to 255 field names or parameters.</span></span> <span data-ttu-id="99c85-116">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="99c85-116">For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="99c85-117">Pour plus d’informations sur les paramètres, voir [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="99c85-117">For more information on parameters, see [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="99c85-118">*datatype*</span><span class="sxs-lookup"><span data-stu-id="99c85-118">*datatype*</span></span>|<span data-ttu-id="99c85-119">Un des principaux [types de données Microsoft Access SQL](sql-data-types.md) ou un de leurs synonymes.</span><span class="sxs-lookup"><span data-stu-id="99c85-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="99c85-120">*sqlstatement*</span><span class="sxs-lookup"><span data-stu-id="99c85-120">*SQLStatement*</span></span>|<span data-ttu-id="99c85-121">Instruction SQL telle que SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, etc.</span><span class="sxs-lookup"><span data-stu-id="99c85-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="99c85-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="99c85-122">Remarks</span></span>

<span data-ttu-id="99c85-123">Une procédure SQL se compose d’une clause PROCEDURE (spécifiant le nom de la procédure), d’une liste facultative de définitions de paramètres et d’une instruction SQL unique.</span><span class="sxs-lookup"><span data-stu-id="99c85-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="99c85-124">Le nom d’une procédure ne peut pas être identique au nom d’une table existante.</span><span class="sxs-lookup"><span data-stu-id="99c85-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="99c85-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="99c85-125">Example</span></span>

<span data-ttu-id="99c85-126">Cet exemple nomme la requête CategoryList et appelle la procédure EnumFields, que vous pouvez trouver dans l'exemple d'instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="99c85-126">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
