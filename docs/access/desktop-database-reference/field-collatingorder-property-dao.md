---
title: Field.CollatingOrder Property (DAO)
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
ms.openlocfilehash: 3258e19c7e167927cf341089ed99e5525ebb0f8d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868132"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="0a3bd-102">Field.CollatingOrder Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0a3bd-102">Field.CollatingOrder Property (DAO)</span></span>


<span data-ttu-id="0a3bd-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a3bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a3bd-p101">Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur **Long** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0a3bd-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a3bd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a3bd-106">Syntax</span></span>

<span data-ttu-id="0a3bd-107">*expression* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="0a3bd-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="0a3bd-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="0a3bd-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a3bd-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="0a3bd-109">Remarks</span></span>

<span data-ttu-id="0a3bd-110">La valeur de retour est une valeur de type **Long** ou une constante pouvant avoir l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0a3bd-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a3bd-111">Constante</span><span class="sxs-lookup"><span data-stu-id="0a3bd-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="0a3bd-112">Ordre de tri</span><span class="sxs-lookup"><span data-stu-id="0a3bd-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-114">Général (Anglais, Français, Allemand, Portugais, Italien et Espagnol moderne)</span><span class="sxs-lookup"><span data-stu-id="0a3bd-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-116">Arabe</span><span class="sxs-lookup"><span data-stu-id="0a3bd-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-118">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="0a3bd-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-120">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="0a3bd-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-122">Russe</span><span class="sxs-lookup"><span data-stu-id="0a3bd-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-124">Tchèque</span><span class="sxs-lookup"><span data-stu-id="0a3bd-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-126">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="0a3bd-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-128">Grec</span><span class="sxs-lookup"><span data-stu-id="0a3bd-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-130">Hébreu</span><span class="sxs-lookup"><span data-stu-id="0a3bd-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-132">Hongrois</span><span class="sxs-lookup"><span data-stu-id="0a3bd-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-134">Islandais</span><span class="sxs-lookup"><span data-stu-id="0a3bd-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-136">Japonais</span><span class="sxs-lookup"><span data-stu-id="0a3bd-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-138">Coréen</span><span class="sxs-lookup"><span data-stu-id="0a3bd-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-140">Neutre</span><span class="sxs-lookup"><span data-stu-id="0a3bd-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-142">Norvégien ou Danois</span><span class="sxs-lookup"><span data-stu-id="0a3bd-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-144">International Paradox</span><span class="sxs-lookup"><span data-stu-id="0a3bd-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-146">Norvégien ou Danois Paradox</span><span class="sxs-lookup"><span data-stu-id="0a3bd-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-148">Suédois ou Finnois Paradox</span><span class="sxs-lookup"><span data-stu-id="0a3bd-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-150">Polonais</span><span class="sxs-lookup"><span data-stu-id="0a3bd-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-152">Slovène</span><span class="sxs-lookup"><span data-stu-id="0a3bd-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-154">Espagnol</span><span class="sxs-lookup"><span data-stu-id="0a3bd-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-156">Suédois ou Finnois</span><span class="sxs-lookup"><span data-stu-id="0a3bd-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-158">Thaï</span><span class="sxs-lookup"><span data-stu-id="0a3bd-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-160">Turc</span><span class="sxs-lookup"><span data-stu-id="0a3bd-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="0a3bd-162">Non défini ou inconnu</span><span class="sxs-lookup"><span data-stu-id="0a3bd-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a3bd-163">La disponibilité de la propriété **CollatingOrder** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0a3bd-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a3bd-164">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="0a3bd-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="0a3bd-165">Alors CollatingOrder est</span><span class="sxs-lookup"><span data-stu-id="0a3bd-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-166">objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3bd-167">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a3bd-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-168">							objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3bd-169">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a3bd-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-170">							objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3bd-171">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a3bd-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3bd-172">							objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3bd-173">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a3bd-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3bd-174">objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="0a3bd-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3bd-175">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a3bd-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a3bd-176">Le paramètre de propriété **CollatingOrder** correspond à l’argument paramètres régionaux de la méthode **CreateDatabase** lors de la création de la base de données ou de la méthode **CompactDatabase** lors du dernier compactage de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0a3bd-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="0a3bd-p102">Les paramètres de propriété **CollatingOrder** et **Attributes** d'un objet **Field** d'une collection **Fields** d'un objet **Index** déterminent ensemble la séquence et la direction de l'ordre de tri dans un index. Toutefois, vous ne pouvez définir aucun ordre de tri pour un index individuel, vous pouvez uniquement le faire pour une table entière.</span><span class="sxs-lookup"><span data-stu-id="0a3bd-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

