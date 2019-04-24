---
title: QueryDef. MaxRecords, propriété (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6738762ba18289293c67392d47e278066ead071d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301077"
---
# <a name="querydefmaxrecords-property-dao"></a><span data-ttu-id="e4bfe-102">QueryDef. MaxRecords, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="e4bfe-102">QueryDef.MaxRecords property (DAO)</span></span>

<span data-ttu-id="e4bfe-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4bfe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4bfe-104">Définit ou renvoie le nombre maximum d'enregistrements à renvoyer pour une requête sur une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-104">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4bfe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4bfe-105">Syntax</span></span>

<span data-ttu-id="e4bfe-106">*expression* . MaxRecords</span><span class="sxs-lookup"><span data-stu-id="e4bfe-106">*expression* .MaxRecords</span></span>

<span data-ttu-id="e4bfe-107">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="e4bfe-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4bfe-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="e4bfe-108">Remarks</span></span>

<span data-ttu-id="e4bfe-109">La valeur par défaut est 0, indiquant que le nombre d'enregistrements renvoyés est illimité.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-109">The default value is 0, indicating no limit on the number of records returned.</span></span>

<span data-ttu-id="e4bfe-p101">Une fois que le nombre de lignes spécifié par **MaxRecords** est renvoyé à votre application dans un objet **[Recordset](recordset-object-dao.md)**, le gestionnaire de requêtes arrête son traitement même si d'autres enregistrements pourraient être inclus dans l'objet **Recordset**. Cette propriété est utile dans les cas où les ressources client limitées empêchent la gestion de grandes quantités d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-p101">Once the number of rows specified by **MaxRecords** is returned to your application in a **[Recordset](recordset-object-dao.md)**, the query processor will stop returning additional records even if more records would qualify for inclusion in the **Recordset**. This property is useful in situations where limited client resources prohibit management of large numbers of records.</span></span>

> [!NOTE]
> <span data-ttu-id="e4bfe-112">[!REMARQUE] La propriété **MaxRecords** est compatible uniquement avec une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-112">The **MaxRecords** property can only be used with an ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="e4bfe-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4bfe-113">Example</span></span>

<span data-ttu-id="e4bfe-114">Cet exemple utilise la propriété **MaxRecords** pour limiter le nombre maximal des enregistrements renvoyés par une requête sur une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-114">This example uses the **MaxRecords** property to set a limit on how many records are returned by a query on an ODBC data source.</span></span>

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

