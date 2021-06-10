---
title: Field.CollatingOrder, propriété (DAO)
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
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="e13fd-102">Field.CollatingOrder, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="e13fd-102">Field.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="e13fd-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e13fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e13fd-p101">Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur **Long** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e13fd-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13fd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e13fd-106">Syntax</span></span>

<span data-ttu-id="e13fd-107">*.* CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="e13fd-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="e13fd-108">*expression* Variable qui représente un objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="e13fd-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e13fd-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="e13fd-109">Remarks</span></span>

<span data-ttu-id="e13fd-110">La valeur de retour est une valeur de type **Long** ou une constante pouvant avoir l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e13fd-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e13fd-111">Constante</span><span class="sxs-lookup"><span data-stu-id="e13fd-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="e13fd-112">Ordre de tri</span><span class="sxs-lookup"><span data-stu-id="e13fd-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-114">Général (Anglais, Français, Allemand, Portugais, Italien et Espagnol moderne)</span><span class="sxs-lookup"><span data-stu-id="e13fd-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-116">Arabe</span><span class="sxs-lookup"><span data-stu-id="e13fd-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-118">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="e13fd-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-120">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="e13fd-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-122">Russe</span><span class="sxs-lookup"><span data-stu-id="e13fd-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-124">Tchèque</span><span class="sxs-lookup"><span data-stu-id="e13fd-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-126">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="e13fd-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-128">Grec</span><span class="sxs-lookup"><span data-stu-id="e13fd-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-130">Hébreu</span><span class="sxs-lookup"><span data-stu-id="e13fd-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-131"><strong>dbSortHungungung</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-132">Hongrois</span><span class="sxs-lookup"><span data-stu-id="e13fd-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-134">Islandais</span><span class="sxs-lookup"><span data-stu-id="e13fd-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-136">Japanese</span><span class="sxs-lookup"><span data-stu-id="e13fd-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-138">Korean</span><span class="sxs-lookup"><span data-stu-id="e13fd-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-140">Neutre</span><span class="sxs-lookup"><span data-stu-id="e13fd-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-142">Norvégien ou Danois</span><span class="sxs-lookup"><span data-stu-id="e13fd-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-144">International Paradox</span><span class="sxs-lookup"><span data-stu-id="e13fd-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-146">Norvégien ou Danois Paradox</span><span class="sxs-lookup"><span data-stu-id="e13fd-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-148">Suédois ou Finnois Paradox</span><span class="sxs-lookup"><span data-stu-id="e13fd-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-150">Polonais</span><span class="sxs-lookup"><span data-stu-id="e13fd-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-152">Slovène</span><span class="sxs-lookup"><span data-stu-id="e13fd-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-154">Espagnol</span><span class="sxs-lookup"><span data-stu-id="e13fd-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-156">Suédois ou Finnois</span><span class="sxs-lookup"><span data-stu-id="e13fd-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-158">Thaï</span><span class="sxs-lookup"><span data-stu-id="e13fd-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-160">Turc</span><span class="sxs-lookup"><span data-stu-id="e13fd-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fd-162">Non défini ou inconnu</span><span class="sxs-lookup"><span data-stu-id="e13fd-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e13fd-163">La disponibilité de la propriété **CollatingOrder** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e13fd-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e13fd-164">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="e13fd-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="e13fd-165">Alors CollatingOrder est</span><span class="sxs-lookup"><span data-stu-id="e13fd-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-166">objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e13fd-167">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="e13fd-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-168">objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e13fd-169">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e13fd-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-170">objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e13fd-171">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e13fd-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fd-172">objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e13fd-173">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="e13fd-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fd-174">objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="e13fd-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e13fd-175">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e13fd-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e13fd-176">Le paramètre de la propriété **CollatingOrder** correspond à l’argument de paramètres régionaux de la méthode **CreateDatabase** lors de la création de la base de données ou à la méthode **CompactDatabase** lors du dernier compactage de la base de données.</span><span class="sxs-lookup"><span data-stu-id="e13fd-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="e13fd-p102">Les paramètres de propriété **CollatingOrder** et **Attributes** d'un objet **Field** d'une collection **Fields** d'un objet **Index** déterminent ensemble la séquence et la direction de l'ordre de tri dans un index. Toutefois, vous ne pouvez définir aucun ordre de tri pour un index individuel, vous pouvez uniquement le faire pour une table entière.</span><span class="sxs-lookup"><span data-stu-id="e13fd-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

