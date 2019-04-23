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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288510"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="49046-102">Fonctions scalaires ODBC</span><span class="sxs-lookup"><span data-stu-id="49046-102">ODBC scalar functions</span></span>

<span data-ttu-id="49046-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49046-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49046-104">Microsoft Access SQL prend en charge l'utilisation de la syntaxe définie par ODBC pour les fonctions scalaires.</span><span class="sxs-lookup"><span data-stu-id="49046-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="49046-105">Par exemple, la requête `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` renvoie toutes les lignes où la valeur absolue de la modification du prix d'une action était supérieure à cinq.</span><span class="sxs-lookup"><span data-stu-id="49046-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="49046-p101">Un sous-ensemble des fonctions scalaires ODBC est pris en charge. La tableau suivant répertorie les fonctions prises en charge.</span><span class="sxs-lookup"><span data-stu-id="49046-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="49046-108">Pour une description des arguments et une explication complète de la syntaxe d'échappement permettant d'inclure des fonctions dans une instruction SQL, consultez la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="49046-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="49046-109">Fonctions de chaîne</span><span class="sxs-lookup"><span data-stu-id="49046-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49046-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="49046-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="49046-111">LAPS</span><span class="sxs-lookup"><span data-stu-id="49046-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="49046-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="49046-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49046-113">ÉCHELLE</span><span class="sxs-lookup"><span data-stu-id="49046-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="49046-114">REPÉRER</span><span class="sxs-lookup"><span data-stu-id="49046-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="49046-115">ESPACE</span><span class="sxs-lookup"><span data-stu-id="49046-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49046-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="49046-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="49046-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="49046-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="49046-118">SOUS-chaîne</span><span class="sxs-lookup"><span data-stu-id="49046-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49046-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="49046-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="49046-120">Oui</span><span class="sxs-lookup"><span data-stu-id="49046-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="49046-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="49046-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49046-122">RENSEIGNÉ</span><span class="sxs-lookup"><span data-stu-id="49046-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="49046-123">Fonctions numériques</span><span class="sxs-lookup"><span data-stu-id="49046-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49046-124">ABS</span><span class="sxs-lookup"><span data-stu-id="49046-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="49046-125">CHAUSSÉE</span><span class="sxs-lookup"><span data-stu-id="49046-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="49046-126">SINE</span><span class="sxs-lookup"><span data-stu-id="49046-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49046-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="49046-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="49046-128">ROUVRIR</span><span class="sxs-lookup"><span data-stu-id="49046-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="49046-129">COMPLEXE</span><span class="sxs-lookup"><span data-stu-id="49046-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49046-130">ENCASTRE</span><span class="sxs-lookup"><span data-stu-id="49046-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="49046-131">CONSOMMATION</span><span class="sxs-lookup"><span data-stu-id="49046-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="49046-132">TAN</span><span class="sxs-lookup"><span data-stu-id="49046-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49046-133">SINU</span><span class="sxs-lookup"><span data-stu-id="49046-133">COS</span></span></p></td>
<td><p><span data-ttu-id="49046-134">VÉRIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="49046-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="49046-135">MSSQL</span><span class="sxs-lookup"><span data-stu-id="49046-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49046-136">PRÉVU</span><span class="sxs-lookup"><span data-stu-id="49046-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="49046-137">INSCRIV</span><span class="sxs-lookup"><span data-stu-id="49046-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="49046-138">Fonctions de date et d'heure &</span><span class="sxs-lookup"><span data-stu-id="49046-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49046-139">CAILLÉ</span><span class="sxs-lookup"><span data-stu-id="49046-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="49046-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="49046-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="49046-141">SEMESTRIELLE</span><span class="sxs-lookup"><span data-stu-id="49046-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49046-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="49046-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="49046-143">AUTRE</span><span class="sxs-lookup"><span data-stu-id="49046-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="49046-144">MENSUEL</span><span class="sxs-lookup"><span data-stu-id="49046-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49046-145">F1</span><span class="sxs-lookup"><span data-stu-id="49046-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="49046-146">H/24</span><span class="sxs-lookup"><span data-stu-id="49046-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="49046-147">TRIMESTRE</span><span class="sxs-lookup"><span data-stu-id="49046-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49046-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="49046-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="49046-149">PRÉCÉDENTE</span><span class="sxs-lookup"><span data-stu-id="49046-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="49046-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="49046-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49046-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="49046-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="49046-152">SECONDE</span><span class="sxs-lookup"><span data-stu-id="49046-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="49046-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="49046-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="49046-154">Conversion de type de données</span><span class="sxs-lookup"><span data-stu-id="49046-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49046-155">REMPLACER</span><span class="sxs-lookup"><span data-stu-id="49046-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="49046-156">Les littéraux de chaîne peuvent être convertis dans les types de données suivants : SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR et SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="49046-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

