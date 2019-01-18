---
title: Fonctions scalaires ODBC
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718034"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="261f4-102">Fonctions scalaires ODBC</span><span class="sxs-lookup"><span data-stu-id="261f4-102">ODBC scalar functions</span></span>

<span data-ttu-id="261f4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="261f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="261f4-104">Microsoft Access SQL prend en charge l’utilisation de la syntaxe définie par ODBC pour les fonctions scalaires.</span><span class="sxs-lookup"><span data-stu-id="261f4-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="261f4-105">Par exemple, la requête `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` renverrait toutes les lignes où la valeur absolue de la modification du prix d’une action serait supérieure à cinq.</span><span class="sxs-lookup"><span data-stu-id="261f4-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="261f4-p101">Un sous-ensemble des fonctions scalaires ODBC est pris en charge. La tableau suivant répertorie les fonctions prises en charge.</span><span class="sxs-lookup"><span data-stu-id="261f4-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="261f4-108">Pour une description des arguments et une explication complète de la syntaxe d'échappement permettant d'inclure des fonctions dans une instruction SQL, consultez la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="261f4-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="261f4-109">Fonctions de chaîne</span><span class="sxs-lookup"><span data-stu-id="261f4-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="261f4-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="261f4-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="261f4-111">LENGTH</span><span class="sxs-lookup"><span data-stu-id="261f4-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="261f4-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="261f4-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="261f4-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="261f4-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="261f4-114">LOCATE</span><span class="sxs-lookup"><span data-stu-id="261f4-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="261f4-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="261f4-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="261f4-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="261f4-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="261f4-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="261f4-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="261f4-118">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="261f4-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="261f4-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="261f4-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="261f4-120">RIGHT</span><span class="sxs-lookup"><span data-stu-id="261f4-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="261f4-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="261f4-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="261f4-122">LEFT</span><span class="sxs-lookup"><span data-stu-id="261f4-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="261f4-123">Fonctions numériques</span><span class="sxs-lookup"><span data-stu-id="261f4-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="261f4-124">ABS</span><span class="sxs-lookup"><span data-stu-id="261f4-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="261f4-125">FLOOR</span><span class="sxs-lookup"><span data-stu-id="261f4-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="261f4-126">SIN</span><span class="sxs-lookup"><span data-stu-id="261f4-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="261f4-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="261f4-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="261f4-128">LOG</span><span class="sxs-lookup"><span data-stu-id="261f4-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="261f4-129">SQRT</span><span class="sxs-lookup"><span data-stu-id="261f4-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="261f4-130">CEILING</span><span class="sxs-lookup"><span data-stu-id="261f4-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="261f4-131">POWER</span><span class="sxs-lookup"><span data-stu-id="261f4-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="261f4-132">TAN</span><span class="sxs-lookup"><span data-stu-id="261f4-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="261f4-133">COS</span><span class="sxs-lookup"><span data-stu-id="261f4-133">COS</span></span></p></td>
<td><p><span data-ttu-id="261f4-134">RAND</span><span class="sxs-lookup"><span data-stu-id="261f4-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="261f4-135">MOD</span><span class="sxs-lookup"><span data-stu-id="261f4-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="261f4-136">EXP</span><span class="sxs-lookup"><span data-stu-id="261f4-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="261f4-137">SIGN</span><span class="sxs-lookup"><span data-stu-id="261f4-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="261f4-138">Fonctions de Date &</span><span class="sxs-lookup"><span data-stu-id="261f4-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="261f4-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="261f4-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="261f4-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="261f4-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="261f4-141">MONTH</span><span class="sxs-lookup"><span data-stu-id="261f4-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="261f4-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="261f4-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="261f4-143">YEAR</span><span class="sxs-lookup"><span data-stu-id="261f4-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="261f4-144">WEEK</span><span class="sxs-lookup"><span data-stu-id="261f4-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="261f4-145">NOW</span><span class="sxs-lookup"><span data-stu-id="261f4-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="261f4-146">HOUR</span><span class="sxs-lookup"><span data-stu-id="261f4-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="261f4-147">QUARTER</span><span class="sxs-lookup"><span data-stu-id="261f4-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="261f4-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="261f4-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="261f4-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="261f4-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="261f4-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="261f4-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="261f4-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="261f4-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="261f4-152">SECOND</span><span class="sxs-lookup"><span data-stu-id="261f4-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="261f4-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="261f4-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="261f4-154">Conversion de type de données</span><span class="sxs-lookup"><span data-stu-id="261f4-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="261f4-155">CONVERT</span><span class="sxs-lookup"><span data-stu-id="261f4-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="261f4-156">Les littéraux de chaîne peuvent être convertis dans les types de données suivants : SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR et SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="261f4-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

