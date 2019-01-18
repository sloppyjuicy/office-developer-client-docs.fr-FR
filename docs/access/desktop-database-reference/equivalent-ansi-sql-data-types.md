---
title: Types de données équivalents ANSI SQL
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699379"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="9ec30-102">Types de données équivalents ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="9ec30-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="9ec30-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ec30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ec30-104">Le tableau suivant répertorie les types de données ANSI SQL, leurs équivalents SQL du moteur de base de données Microsoft Access et leurs synonymes valides.</span><span class="sxs-lookup"><span data-stu-id="9ec30-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="9ec30-105">Il indique également les types de données Microsoft SQL Server™ équivalentes.</span><span class="sxs-lookup"><span data-stu-id="9ec30-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ec30-106">Type de données ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="9ec30-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="9ec30-107">Type de données Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="9ec30-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="9ec30-108">
Synonyme</span><span class="sxs-lookup"><span data-stu-id="9ec30-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="9ec30-109">Type de données Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="9ec30-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec30-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="9ec30-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="9ec30-111">BINARY (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9ec30-112">VARBINARY, BINARY VARYING BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="9ec30-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="9ec30-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="9ec30-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec30-114">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="9ec30-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="9ec30-115">BIT (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9ec30-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="9ec30-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="9ec30-117">BIT</span><span class="sxs-lookup"><span data-stu-id="9ec30-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec30-118">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="9ec30-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="9ec30-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="9ec30-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="9ec30-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="9ec30-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="9ec30-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="9ec30-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec30-122">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="9ec30-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="9ec30-123">COUNTER (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9ec30-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="9ec30-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="9ec30-125">(voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec30-126">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="9ec30-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="9ec30-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="9ec30-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="9ec30-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="9ec30-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="9ec30-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="9ec30-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec30-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="9ec30-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="9ec30-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="9ec30-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="9ec30-132">DATE, TIME (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9ec30-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="9ec30-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec30-134">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="9ec30-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="9ec30-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="9ec30-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="9ec30-136">GUID</span><span class="sxs-lookup"><span data-stu-id="9ec30-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="9ec30-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="9ec30-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec30-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="9ec30-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="9ec30-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="9ec30-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="9ec30-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="9ec30-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="9ec30-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="9ec30-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec30-142">REAL</span><span class="sxs-lookup"><span data-stu-id="9ec30-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="9ec30-143">REAL</span><span class="sxs-lookup"><span data-stu-id="9ec30-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="9ec30-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="9ec30-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="9ec30-145">REAL</span><span class="sxs-lookup"><span data-stu-id="9ec30-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec30-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="9ec30-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="9ec30-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9ec30-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="9ec30-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9ec30-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9ec30-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec30-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="9ec30-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="9ec30-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="9ec30-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="9ec30-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="9ec30-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="9ec30-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="9ec30-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec30-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="9ec30-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="9ec30-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="9ec30-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="9ec30-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="9ec30-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="9ec30-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="9ec30-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec30-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="9ec30-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="9ec30-159">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="9ec30-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="9ec30-160">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="9ec30-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec30-161">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="9ec30-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="9ec30-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="9ec30-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="9ec30-163">LONGBINARY, GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="9ec30-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="9ec30-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="9ec30-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec30-165">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="9ec30-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="9ec30-166">TEXTE (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9ec30-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9ec30-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="9ec30-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec30-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="9ec30-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="9ec30-170">CHAR (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9ec30-171">Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9ec30-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9ec30-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="9ec30-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="9ec30-p102">Le type de données BIT ANSI SQL ne correspond pas au type de données BIT Microsoft Access SQL. En revanche, il correspond au type de données BINARY. Il n'existe aucun équivalent ANSI SQL pour le type de données BIT Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="9ec30-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="9ec30-176">TIMESTAMP n'est plus reconnu comme synonyme de DATETIME.</span><span class="sxs-lookup"><span data-stu-id="9ec30-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="9ec30-p103">NUMERIC n'est plus reconnu comme synonyme de FLOAT ou DOUBLE. NUMERIC est désormais utilisé comme synonyme de DECIMAL.</span><span class="sxs-lookup"><span data-stu-id="9ec30-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="9ec30-179">Un champ LONGTEXT est toujours stocké dans le format de représentation Unicode.</span><span class="sxs-lookup"><span data-stu-id="9ec30-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="9ec30-p104">Si le nom du type de données TEXT est utilisé sans que la longueur facultative soit spécifiée, par exemple TEXT(25), un champ LONGTEXT est créé. Des [instructions CREATE TABLE](create-table-statement-microsoft-access-sql.md) sont alors créées pour produire des types de données cohérents avec Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9ec30-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="9ec30-182">Un champ CHAR est toujours stocké dans le format de représentation Unicode qui est l'équivalent du type de données NATIONAL CHAR ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="9ec30-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="9ec30-p105">Si le nom du type de données TEXT est utilisé et si la longueur facultative est spécifiée, par exemple TEXT(25), le type de données du champ est équivalent au type de données CHAR. Ceci permet d'assurer la compatibilité avec les anciennes versions de la plupart des applications Microsoft Jet et d'aligner le type de données TEXT (sans spécification de longueur) avec Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9ec30-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


