---
title: Fonctions d'agrégation SQL (SQL)
TOCTitle: SQL Aggregate Functions (SQL)
ms:assetid: 8866cd71-0216-25b4-6a6a-02cb7acad9a2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197054(v=office.15)
ms:contentKeyID: 48546136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fd06b02d4331a51e0f8a186f713d80d98bbed20
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870561"
---
# <a name="sql-aggregate-functions-sql"></a><span data-ttu-id="8aecf-102">Fonctions d'agrégation SQL (SQL)</span><span class="sxs-lookup"><span data-stu-id="8aecf-102">SQL Aggregate Functions (SQL)</span></span>


<span data-ttu-id="8aecf-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8aecf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8aecf-p101">Les fonctions d'agrégation SQL permettent d'effectuer diverses opérations statistiques sur des ensembles de valeurs. Vous pouvez les utiliser dans une requête ou dans des expressions d'agrégation de la propriété **SQL** d'un objet **QueryDef** ou lors de la création d'un objet **Recordset** en fonction d'une requête SQL.</span><span class="sxs-lookup"><span data-stu-id="8aecf-p101">Using the SQL aggregate functions, you can determine various statistics on sets of values. You can use these functions in a query and aggregate expressions in the **SQL** property of a **QueryDef** object or when creating a **Recordset** object based on an SQL query.</span></span>

<span data-ttu-id="8aecf-106">**[Avg, fonction](https://msdn.microsoft.com/library/ff822755\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="8aecf-106">**[Avg Function](https://msdn.microsoft.com/library/ff822755\(v=office.15\))**</span></span>

<span data-ttu-id="8aecf-107">**[Count, fonction](https://msdn.microsoft.com/library/ff844748\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="8aecf-107">**[Count Function](https://msdn.microsoft.com/library/ff844748\(v=office.15\))**</span></span>

<span data-ttu-id="8aecf-108">**[First, Last, fonctions](https://msdn.microsoft.com/library/ff197381\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="8aecf-108">**[First, Last Functions](https://msdn.microsoft.com/library/ff197381\(v=office.15\))**</span></span>

<span data-ttu-id="8aecf-109">**[Min, Max, fonctions](https://msdn.microsoft.com/library/ff194490\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="8aecf-109">**[Min, Max Functions](https://msdn.microsoft.com/library/ff194490\(v=office.15\))**</span></span>

<span data-ttu-id="8aecf-110">**[StDev, StDevP, fonctions](https://msdn.microsoft.com/library/ff197043\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="8aecf-110">**[StDev, StDevP Functions](https://msdn.microsoft.com/library/ff197043\(v=office.15\))**</span></span>

<span data-ttu-id="8aecf-111">**[Sum, fonction](https://msdn.microsoft.com/library/ff844764\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="8aecf-111">**[Sum Function](https://msdn.microsoft.com/library/ff844764\(v=office.15\))**</span></span>

<span data-ttu-id="8aecf-112">**[Var, VarP, fonctions](https://msdn.microsoft.com/library/ff192105\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="8aecf-112">**[Var, VarP Functions](https://msdn.microsoft.com/library/ff192105\(v=office.15\))**</span></span>

