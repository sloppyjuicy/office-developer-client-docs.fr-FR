---
title: Déclaration PARAMETERS (Microsoft Access SQL)
TOCTitle: PARAMETERS declaration (Microsoft Access SQL)
ms:assetid: 0dcaad68-6a5f-93dc-e62a-b82b36e1e69c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845220(v=office.15)
ms:contentKeyID: 48543230
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277577
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 64e40da96dc6d82c0f682cba5a3ebc7cfb82bb50
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026406"
---
# <a name="parameters-declaration-microsoft-access-sql"></a><span data-ttu-id="e4ed7-102">Déclaration PARAMETERS (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e4ed7-102">PARAMETERS declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="e4ed7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4ed7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4ed7-104">Déclare le nom et le type de données de chaque paramètre d'une requête Paramètre.</span><span class="sxs-lookup"><span data-stu-id="e4ed7-104">Declares the name and data type of each parameter in a parameter query.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ed7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4ed7-105">Syntax</span></span>

<span data-ttu-id="e4ed7-106">PARAMETERS *nom typedonnées* \[, *nom typedonnées* \[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="e4ed7-106">PARAMETERS *name datatype* \[, *name datatype* \[, …\]\]</span></span>

<span data-ttu-id="e4ed7-107">La déclaration PARAMETERS est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e4ed7-107">The PARAMETERS declaration has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4ed7-108">Argument</span><span class="sxs-lookup"><span data-stu-id="e4ed7-108">Part</span></span></p></th>
<th><p><span data-ttu-id="e4ed7-109">Description</span><span class="sxs-lookup"><span data-stu-id="e4ed7-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4ed7-110"><em>nom</em></span><span class="sxs-lookup"><span data-stu-id="e4ed7-110"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="e4ed7-111">Nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="e4ed7-111">The name of the parameter.</span></span> <span data-ttu-id="e4ed7-112">Affecté à la propriété <strong>Name</strong> de l'objet <strong>Parameter</strong> et servant à identifier ce paramètre dans la collection <strong>Parameters</strong>.</span><span class="sxs-lookup"><span data-stu-id="e4ed7-112">Assigned to the <strong>Name</strong> property of the <strong>Parameter</strong> object and used to identify this parameter in the <strong>Parameters</strong> collection.</span></span> <span data-ttu-id="e4ed7-113">Vous pouvez utiliser le <em>nom</em> sous forme de chaîne qui est affichée dans une boîte de dialogue pendant que votre application exécute la requête.</span><span class="sxs-lookup"><span data-stu-id="e4ed7-113">You can use <em>name</em> as a string that is displayed in a dialog box while your application runs the query.</span></span> <span data-ttu-id="e4ed7-114">Utilisez des crochets ([ ]) pour encadrer les textes contenant des espaces ou des signes de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="e4ed7-114">Use brackets ([ ]) to enclose text that contains spaces or punctuation.</span></span> <span data-ttu-id="e4ed7-115">Par exemple, [prix bas] et [lancer l’état avec les month?] sont des arguments valides de <em>nom</em> .</span><span class="sxs-lookup"><span data-stu-id="e4ed7-115">For example, [Low price] and [Begin report with which month?] are valid <em>name</em> arguments.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4ed7-116"><em>typedonnées</em></span><span class="sxs-lookup"><span data-stu-id="e4ed7-116"><em>datatype</em></span></span></p></td>
<td><p><span data-ttu-id="e4ed7-117">Un des principaux <a href="sql-data-types.md">types de données Microsoft Access SQL</a> ou un de leurs synonymes.</span><span class="sxs-lookup"><span data-stu-id="e4ed7-117">One of the primary <a href="sql-data-types.md">Microsoft Access SQL data types</a> or their synonyms.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e4ed7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e4ed7-118">Remarks</span></span>

<span data-ttu-id="e4ed7-p102">Pour les requêtes que vous exécutez régulièrement, vous pouvez utiliser une déclaration PARAMETERS pour créer une requête Paramètre. La création d'une requête Paramètre peut faciliter l'automatisation du processus de modification des critères de requête. Avec une requête Paramètre, votre code devra fournir les paramètres à chaque exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="e4ed7-p102">For queries that you run regularly, you can use a PARAMETERS declaration to create a parameter query. A parameter query can help automate the process of changing query criteria. With a parameter query, your code will need to provide the parameters each time the query is run.</span></span>

<span data-ttu-id="e4ed7-122">La déclaration PARAMETERS est facultative mais précède, lorsqu'elle est incluse, toute autre instruction, y compris l'instruction [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="e4ed7-122">The PARAMETERS declaration is optional but when included precedes any other statement, including [SELECT](select-statement-microsoft-access-sql.md).</span></span>

<span data-ttu-id="e4ed7-p103">Si la déclaration implique plusieurs paramètres, séparez-les par des virgules. Dans l'exemple qui suit, les paramètres sont au nombre de deux :</span><span class="sxs-lookup"><span data-stu-id="e4ed7-p103">If the declaration includes more than one parameter, separate them with commas. The following example includes two parameters:</span></span>

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

<span data-ttu-id="e4ed7-125">Vous pouvez utiliser *nom* mais pas le *type de données* dans une clause [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) ou [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) .</span><span class="sxs-lookup"><span data-stu-id="e4ed7-125">You can use *name* but not *datatype* in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) clause.</span></span> <span data-ttu-id="e4ed7-126">L'exemple suivant attend deux paramètres, puis applique les critères aux enregistrements de la table Orders :</span><span class="sxs-lookup"><span data-stu-id="e4ed7-126">The following example expects two parameters to be provided and then applies the criteria to records in the Orders table:</span></span>

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a><span data-ttu-id="e4ed7-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4ed7-127">Example</span></span>

<span data-ttu-id="e4ed7-128">Dans l'exemple suivant, l'utilisateur doit fournir un nom de poste qui est ensuite utilisé comme critère de la requête.</span><span class="sxs-lookup"><span data-stu-id="e4ed7-128">This example requires the user to provide a job title and then uses that job title as the criteria for the query.</span></span>

<span data-ttu-id="e4ed7-129">Il appelle la procédure EnumFields que vous pouvez trouver dans l’exemple [d’instruction SELECT](select-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="e4ed7-129">It calls the EnumFields procedure, which you can find in the [SELECT statement](select-statement-microsoft-access-sql.md) example.</span></span>

```vb
    Sub ParametersX() 
     
        Dim dbs As Database, qdf As QueryDef 
        Dim rst As Recordset 
        Dim strSql As String, strParm As String 
        Dim strMessage As String 
        Dim intCommand As Integer 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("NorthWind.mdb") 
         
        ' Define the parameters clause. 
        strParm = "PARAMETERS [Employee Title] CHAR; " 
     
        ' Define an SQL statement with the parameters 
        ' clause. 
        strSql = strParm & "SELECT LastName, FirstName, " _ 
            & "EmployeeID " _ 
            & "FROM Employees " _ 
            & "WHERE Title =[Employee Title];" 
         
        ' Create a QueryDef object based on the  
        ' SQL statement. 
        Set qdf = dbs.CreateQueryDef _ 
            ("Find Employees", strSql) 
         
        Do While True 
            strMessage = "Find Employees by Job " _ 
                & "title:" & Chr(13) _ 
                & "  Choose Job Title:" & Chr(13) _ 
                & "   1 - Sales Manager" & Chr(13) _ 
                & "   2 - Sales Representative" & Chr(13) _ 
                & "   3 - Inside Sales Coordinator" 
             
            intCommand = Val(InputBox(strMessage)) 
             
            Select Case intCommand 
                Case 1 
                    qdf("Employee Title") = _ 
                        "Sales Manager" 
                Case 2 
                    qdf("Employee Title") = _ 
                        "Sales Representative" 
                Case 3 
                    qdf("Employee Title") = _ 
                        "Inside Sales Coordinator" 
                Case Else 
                    Exit Do 
            End Select 
             
            ' Create a temporary snapshot-type Recordset. 
            Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
            ' Populate the Recordset. 
            rst.MoveLast 
                 
            ' Call EnumFields to print the contents of the  
            ' Recordset. Pass the Recordset object and desired 
            ' field width. 
            EnumFields rst, 12 
     
        Loop 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "Find Employees" 
         
        dbs.Close 
     
    End Sub
```
