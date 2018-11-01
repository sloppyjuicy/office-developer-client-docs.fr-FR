---
title: Fonctions d'agrégation, fonction CALC et mot clé NEW
TOCTitle: Aggregate Functions, the CALC Function, and the NEW Keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35ee1bff23e1bcf04c1a9fd4cfc807edbd541148
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882377"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="1ecb7-102">Fonctions d'agrégation, fonction CALC et mot clé NEW</span><span class="sxs-lookup"><span data-stu-id="1ecb7-102">Aggregate Functions, the CALC Function, and the NEW Keyword</span></span>


<span data-ttu-id="1ecb7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ecb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ecb7-p101">La mise en forme des données prend en charge les fonctions suivantes. Le nom attribué au chapitre contenant la colonne à manipuler est *alias-chapitre*.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-p101">Data shaping supports the following functions. The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="1ecb7-p102">Un alias-chapitre peut être complètement qualifié et se composer de chaque nom de colonne de chapitre menant au chapitre contenant le *nom-colonne,*, le tout séparé par des points. Par exemple si le chapitre parent, chap1, contient un chapitre enfant, chap2, avec une colonne de montant, mnt, le nom qualifié sera chap1.chap2.mnt.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-p102">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ecb7-108">Fonctions d'agrégation</span><span class="sxs-lookup"><span data-stu-id="1ecb7-108">Aggregate Functions</span></span></p></th>
<th><p><span data-ttu-id="1ecb7-109">Description</span><span class="sxs-lookup"><span data-stu-id="1ecb7-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-110">Somme (<em>alias-chapitre</em>.<em> nom de la colonne</em>)</span><span class="sxs-lookup"><span data-stu-id="1ecb7-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-111">Calcule la somme de toutes les valeurs dans la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-112">AVG (<em>alias-chapitre</em>.<em> nom de la colonne</em>)</span><span class="sxs-lookup"><span data-stu-id="1ecb7-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-113">Calcule la moyenne de toutes les valeurs dans la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-114">MAX (<em>alias-chapitre</em>.<em> nom de la colonne</em>)</span><span class="sxs-lookup"><span data-stu-id="1ecb7-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-115">Calcule la valeur maximale dans la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-116">MIN (<em>alias-chapitre</em>.<em> nom de la colonne</em>)</span><span class="sxs-lookup"><span data-stu-id="1ecb7-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-117">Calcule la valeur minimale dans la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-118">COUNT (<em>alias-chapitre</em>[.<em> nom de la colonne</em>])</span><span class="sxs-lookup"><span data-stu-id="1ecb7-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-p103">Compte le nombre de lignes dans l'alias spécifié. Si une colonne est spécifiée, seules les lignes pour lesquelles cette colonne n'est pas Null, sont comptées.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-121">STDEV (<em>alias-chapitre</em>.<em> nom de la colonne</em>)</span><span class="sxs-lookup"><span data-stu-id="1ecb7-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-122">Calcule l'écart type dans la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-123">TOUT (<em>alias-chapitre</em>.<em> nom de la colonne</em>)</span><span class="sxs-lookup"><span data-stu-id="1ecb7-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-p104">Valeur de la colonne spécifiée. ANY a une valeur prévisible uniquement si la valeur de la colonne est identique pour toutes les lignes du chapitre.
</span><span class="sxs-lookup"><span data-stu-id="1ecb7-p104">A value of the specified column. ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p>

> [!NOTE]
> <span data-ttu-id="1ecb7-126">Si la colonne ne contient pas la même valeur pour toutes les lignes du chapitre, la commande SHAPE retourne de façon arbitraire une des valeurs pour l'utiliser dans la fonction ANY.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-126">If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span>


<p></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ecb7-127">Expression calculée</span><span class="sxs-lookup"><span data-stu-id="1ecb7-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="1ecb7-128">Description</span><span class="sxs-lookup"><span data-stu-id="1ecb7-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-129">CALC(<em>expression</em>)</span><span class="sxs-lookup"><span data-stu-id="1ecb7-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-p105">Calcule une expression arbitraire, mais uniquement sur la ligne de l’objet <strong>Recordset</strong> contenant la fonction CALC. Toute expression utilisant ces <a href="visual-basic-for-applications-functions.md"> fonctions Visual Basic pour Applications (VBA)</a> est autorisée.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ecb7-132">Mot clé NEW</span><span class="sxs-lookup"><span data-stu-id="1ecb7-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="1ecb7-133">Description</span><span class="sxs-lookup"><span data-stu-id="1ecb7-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-134">NOUVEAU <em>type-champ</em> [(<em>largeur</em> | <em>à l’échelle</em> | <em>précision</em> | <em>erreur</em> [, <em>échelle</em> | <em>erreur</em>])]</span><span class="sxs-lookup"><span data-stu-id="1ecb7-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-135">Ajoute une colonne vide de type spécifié à l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ecb7-136">Le type de données du *type-champ* passé avec le mot clé NEW peut être l'un des suivants :</span><span class="sxs-lookup"><span data-stu-id="1ecb7-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ecb7-137">Types de données OLE DB</span><span class="sxs-lookup"><span data-stu-id="1ecb7-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="1ecb7-138">Type(s) de données ADO équivalent(s)</span><span class="sxs-lookup"><span data-stu-id="1ecb7-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="1ecb7-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="1ecb7-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="1ecb7-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="1ecb7-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="1ecb7-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="1ecb7-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="1ecb7-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="1ecb7-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="1ecb7-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="1ecb7-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="1ecb7-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="1ecb7-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="1ecb7-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ecb7-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="1ecb7-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="1ecb7-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="1ecb7-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="1ecb7-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="1ecb7-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="1ecb7-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="1ecb7-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-160">adLongVarBinary adBinary, AdVarBinary,</span><span class="sxs-lookup"><span data-stu-id="1ecb7-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="1ecb7-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-162">adChar, adVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="1ecb7-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="1ecb7-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="1ecb7-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="1ecb7-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="1ecb7-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="1ecb7-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="1ecb7-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="1ecb7-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="1ecb7-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="1ecb7-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="1ecb7-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-173">AVANT DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="1ecb7-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="1ecb7-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ecb7-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="1ecb7-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="1ecb7-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ecb7-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="1ecb7-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="1ecb7-178">adError</span><span class="sxs-lookup"><span data-stu-id="1ecb7-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ecb7-179">Lorsque le nouveau champ est décimal (dans OLE DB, DBTYPE\_décimal, ou dans ADO, adDecimal), vous devez spécifier les valeurs de précision et une échelle.</span><span class="sxs-lookup"><span data-stu-id="1ecb7-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

