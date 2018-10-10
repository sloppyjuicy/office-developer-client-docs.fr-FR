---
title: Types de données équivalents ANSI SQL
TOCTitle: Equivalent ANSI SQL Data Types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7eae567d2787e60f84c8020d80e1c15c9b02928f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471069"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="a5342-102">Types de données équivalents ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="a5342-102">Equivalent ANSI SQL Data Types</span></span>


<span data-ttu-id="a5342-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5342-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a5342-p101">Le tableau suivant répertorie les types de données ANSI SQL, leurs équivalents SQL du moteur de base de données Microsoft Access et leurs synonymes valides. Il répertorie également les types de données Microsoft® SQL Server équivalents.</span><span class="sxs-lookup"><span data-stu-id="a5342-p101">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms. It also lists the equivalent Microsoft® SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5342-106">Type de données ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="a5342-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="a5342-107">Type de données Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="a5342-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="a5342-108">
Synonyme</span><span class="sxs-lookup"><span data-stu-id="a5342-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="a5342-109">Type de données Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="a5342-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5342-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="a5342-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="a5342-111">BINARY (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a5342-112">VARBINARY, BINARY VARYING BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="a5342-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="a5342-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="a5342-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5342-114">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5342-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="a5342-115">BIT (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a5342-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="a5342-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="a5342-117">BIT</span><span class="sxs-lookup"><span data-stu-id="a5342-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5342-118">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5342-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="a5342-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="a5342-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="a5342-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="a5342-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="a5342-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="a5342-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5342-122">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5342-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="a5342-123">COUNTER (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a5342-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="a5342-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="a5342-125">(voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5342-126">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5342-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="a5342-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="a5342-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="a5342-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="a5342-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="a5342-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="a5342-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5342-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="a5342-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="a5342-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="a5342-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="a5342-132">DATE, TIME (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a5342-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="a5342-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5342-134">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5342-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="a5342-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="a5342-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="a5342-136">GUID</span><span class="sxs-lookup"><span data-stu-id="a5342-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="a5342-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="a5342-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5342-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="a5342-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="a5342-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="a5342-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="a5342-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="a5342-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="a5342-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="a5342-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5342-142">REAL</span><span class="sxs-lookup"><span data-stu-id="a5342-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="a5342-143">REAL</span><span class="sxs-lookup"><span data-stu-id="a5342-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="a5342-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="a5342-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="a5342-145">REAL</span><span class="sxs-lookup"><span data-stu-id="a5342-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5342-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="a5342-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="a5342-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a5342-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="a5342-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a5342-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a5342-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5342-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="a5342-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="a5342-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="a5342-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="a5342-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="a5342-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="a5342-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="a5342-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5342-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="a5342-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="a5342-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="a5342-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="a5342-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="a5342-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="a5342-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="a5342-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5342-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="a5342-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="a5342-159">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5342-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a5342-160">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5342-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5342-161">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5342-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="a5342-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="a5342-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="a5342-163">LONGBINARY, GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="a5342-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="a5342-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="a5342-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5342-165">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5342-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="a5342-166">TEXTE (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a5342-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a5342-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="a5342-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5342-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="a5342-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="a5342-170">CHAR (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a5342-171">Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a5342-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a5342-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="a5342-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="a5342-p102">Le type de données BIT ANSI SQL ne correspond pas au type de données BIT Microsoft Access SQL. En revanche, il correspond au type de données BINARY. Il n'existe aucun équivalent ANSI SQL pour le type de données BIT Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="a5342-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span></P>
> <LI>
> <P><span data-ttu-id="a5342-176">TIMESTAMP n'est plus reconnu comme synonyme de DATETIME.</span><span class="sxs-lookup"><span data-stu-id="a5342-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span></P>
> <LI>
> <P><span data-ttu-id="a5342-p103">NUMERIC n'est plus reconnu comme synonyme de FLOAT ou DOUBLE. NUMERIC est désormais utilisé comme synonyme de DECIMAL.</span><span class="sxs-lookup"><span data-stu-id="a5342-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span></P>
> <LI>
> <P><span data-ttu-id="a5342-179">Un champ LONGTEXT est toujours stocké dans le format de représentation Unicode.</span><span class="sxs-lookup"><span data-stu-id="a5342-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span></P>
> <LI>
> <P><span data-ttu-id="a5342-p104">Si le nom du type de données TEXT est utilisé sans que la longueur facultative soit spécifiée, par exemple TEXT(25), un champ LONGTEXT est créé. Des <A href="create-table-statement-microsoft-access-sql.md">instructions CREATE TABLE</A> sont alors créées pour produire des types de données cohérents avec Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a5342-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables <A href="create-table-statement-microsoft-access-sql.md">CREATE TABLE statements</A> to be written that will yield data types consistent with Microsoft SQL Server.</span></span></P>
> <LI>
> <P><span data-ttu-id="a5342-182">Un champ CHAR est toujours stocké dans le format de représentation Unicode qui est l'équivalent du type de données NATIONAL CHAR ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="a5342-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span></P>
> <LI>
> <P><span data-ttu-id="a5342-p105">Si le nom du type de données TEXT est utilisé et si la longueur facultative est spécifiée, par exemple TEXT(25), le type de données du champ est équivalent au type de données CHAR. Ceci permet d'assurer la compatibilité avec les anciennes versions de la plupart des applications Microsoft Jet et d'aligner le type de données TEXT (sans spécification de longueur) avec Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a5342-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span></P></LI></UL>


