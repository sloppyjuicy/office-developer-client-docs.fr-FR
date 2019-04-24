---
title: Field. CollatingOrder, propriété (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: a2607ace-a660-899b-eae8-4612ce2f87f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820980(v=office.15)
ms:contentKeyID: 48546758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052897
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3d016d779472ec9809d3ac5c77158c2c1d994f3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293125"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="19983-102">Field. CollatingOrder, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="19983-102">Field.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="19983-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19983-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19983-p101">Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur **Long** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="19983-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="19983-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19983-106">Syntax</span></span>

<span data-ttu-id="19983-107">*expression* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="19983-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="19983-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="19983-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="19983-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="19983-109">Remarks</span></span>

<span data-ttu-id="19983-110">La valeur de retour est une valeur de type **Long** ou une constante pouvant avoir l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="19983-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19983-111">Constante</span><span class="sxs-lookup"><span data-stu-id="19983-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="19983-112">Ordre de tri</span><span class="sxs-lookup"><span data-stu-id="19983-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19983-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="19983-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-114">Général (Anglais, Français, Allemand, Portugais, Italien et Espagnol moderne)</span><span class="sxs-lookup"><span data-stu-id="19983-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="19983-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-116">Arabic</span><span class="sxs-lookup"><span data-stu-id="19983-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="19983-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-118">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="19983-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="19983-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-120">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="19983-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="19983-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-122">Russe</span><span class="sxs-lookup"><span data-stu-id="19983-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="19983-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-124">Tchèque</span><span class="sxs-lookup"><span data-stu-id="19983-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="19983-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-126">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="19983-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="19983-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-128">Grec</span><span class="sxs-lookup"><span data-stu-id="19983-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="19983-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-130">Hébreu</span><span class="sxs-lookup"><span data-stu-id="19983-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="19983-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-132">Hongrois</span><span class="sxs-lookup"><span data-stu-id="19983-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="19983-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-134">Islandais</span><span class="sxs-lookup"><span data-stu-id="19983-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="19983-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-136">Japonais</span><span class="sxs-lookup"><span data-stu-id="19983-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="19983-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-138">Coréen</span><span class="sxs-lookup"><span data-stu-id="19983-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="19983-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-140">Neutre</span><span class="sxs-lookup"><span data-stu-id="19983-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="19983-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-142">Norvégien ou Danois</span><span class="sxs-lookup"><span data-stu-id="19983-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="19983-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-144">International Paradox</span><span class="sxs-lookup"><span data-stu-id="19983-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="19983-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-146">Norvégien ou Danois Paradox</span><span class="sxs-lookup"><span data-stu-id="19983-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="19983-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-148">Suédois ou Finnois Paradox</span><span class="sxs-lookup"><span data-stu-id="19983-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="19983-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-150">Polonais</span><span class="sxs-lookup"><span data-stu-id="19983-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="19983-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-152">Slovène</span><span class="sxs-lookup"><span data-stu-id="19983-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="19983-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-154">Espagnol</span><span class="sxs-lookup"><span data-stu-id="19983-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="19983-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-156">Suédois ou Finnois</span><span class="sxs-lookup"><span data-stu-id="19983-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="19983-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-158">Thaï</span><span class="sxs-lookup"><span data-stu-id="19983-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="19983-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-160">Turc</span><span class="sxs-lookup"><span data-stu-id="19983-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="19983-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="19983-162">Non défini ou inconnu</span><span class="sxs-lookup"><span data-stu-id="19983-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="19983-163">La disponibilité de la propriété **CollatingOrder** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="19983-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19983-164">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="19983-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="19983-165">Alors CollatingOrder est</span><span class="sxs-lookup"><span data-stu-id="19983-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19983-166">objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="19983-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="19983-167">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="19983-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-168">objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="19983-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="19983-169">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19983-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-170">objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="19983-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="19983-171">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19983-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19983-172">objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="19983-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="19983-173">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="19983-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19983-174">objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="19983-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="19983-175">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19983-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="19983-176">Le paramètre de la propriété **CollatingOrder** correspond à l'argument paramètres régionaux de la méthode **CreateDatabase** lors de la création de la base de données ou de la méthode **CompactDatabase** lors du dernier compactage de la base de données.</span><span class="sxs-lookup"><span data-stu-id="19983-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="19983-p102">Les paramètres de propriété **CollatingOrder** et **Attributes** d'un objet **Field** d'une collection **Fields** d'un objet **Index** déterminent ensemble la séquence et la direction de l'ordre de tri dans un index. Toutefois, vous ne pouvez définir aucun ordre de tri pour un index individuel, vous pouvez uniquement le faire pour une table entière.</span><span class="sxs-lookup"><span data-stu-id="19983-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

