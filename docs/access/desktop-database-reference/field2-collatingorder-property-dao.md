---
title: Field2.CollatingOrder, propriété (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: cb1d6fc9-a2a6-54c2-abf5-48b609e38738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834380(v=office.15)
ms:contentKeyID: 48547709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02711fbbf39b058bb88e9568716169825ae4a923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292866"
---
# <a name="field2collatingorder-property-dao"></a><span data-ttu-id="6aa62-102">Field2.CollatingOrder, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="6aa62-102">Field2.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="6aa62-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6aa62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6aa62-p101">Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur **Long** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6aa62-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa62-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aa62-106">Syntax</span></span>

<span data-ttu-id="6aa62-107">*.* CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="6aa62-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="6aa62-108">*expression* une variable qui représente une **champ2** objet.</span><span class="sxs-lookup"><span data-stu-id="6aa62-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aa62-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="6aa62-109">Remarks</span></span>

<span data-ttu-id="6aa62-110">La valeur de retour est une valeur de type **Long** ou une constante pouvant avoir l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6aa62-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6aa62-111">Constante</span><span class="sxs-lookup"><span data-stu-id="6aa62-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="6aa62-112">Ordre de tri</span><span class="sxs-lookup"><span data-stu-id="6aa62-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-114">Général (Anglais, Français, Allemand, Portugais, Italien et Espagnol moderne)</span><span class="sxs-lookup"><span data-stu-id="6aa62-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-116">Arabe</span><span class="sxs-lookup"><span data-stu-id="6aa62-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-118">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="6aa62-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-120">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="6aa62-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-122">Russe</span><span class="sxs-lookup"><span data-stu-id="6aa62-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-124">Tchèque</span><span class="sxs-lookup"><span data-stu-id="6aa62-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-126">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="6aa62-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-128">Grec</span><span class="sxs-lookup"><span data-stu-id="6aa62-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-130">Hébreu</span><span class="sxs-lookup"><span data-stu-id="6aa62-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-131"><strong>dbSortHungungung</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-132">Hongrois</span><span class="sxs-lookup"><span data-stu-id="6aa62-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-134">Islandais</span><span class="sxs-lookup"><span data-stu-id="6aa62-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-136">Japanese</span><span class="sxs-lookup"><span data-stu-id="6aa62-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-138">Korean</span><span class="sxs-lookup"><span data-stu-id="6aa62-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-140">Neutre</span><span class="sxs-lookup"><span data-stu-id="6aa62-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-142">Norvégien ou Danois</span><span class="sxs-lookup"><span data-stu-id="6aa62-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-144">International Paradox</span><span class="sxs-lookup"><span data-stu-id="6aa62-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-146">Norvégien ou Danois Paradox</span><span class="sxs-lookup"><span data-stu-id="6aa62-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-148">Suédois ou Finnois Paradox</span><span class="sxs-lookup"><span data-stu-id="6aa62-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-150">Polonais</span><span class="sxs-lookup"><span data-stu-id="6aa62-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-152">Slovène</span><span class="sxs-lookup"><span data-stu-id="6aa62-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-154">Espagnol</span><span class="sxs-lookup"><span data-stu-id="6aa62-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-156">Suédois ou Finnois</span><span class="sxs-lookup"><span data-stu-id="6aa62-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-158">Thaï</span><span class="sxs-lookup"><span data-stu-id="6aa62-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-160">Turc</span><span class="sxs-lookup"><span data-stu-id="6aa62-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="6aa62-162">Non défini ou inconnu</span><span class="sxs-lookup"><span data-stu-id="6aa62-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6aa62-163">La disponibilité de la propriété **CollatingOrder** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6aa62-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6aa62-164">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="6aa62-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="6aa62-165">Alors CollatingOrder est</span><span class="sxs-lookup"><span data-stu-id="6aa62-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-166">objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6aa62-167">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="6aa62-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-168">objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6aa62-169">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6aa62-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-170">objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6aa62-171">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6aa62-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa62-172">objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6aa62-173">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="6aa62-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa62-174">objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="6aa62-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6aa62-175">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6aa62-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6aa62-176">Le paramètre de la propriété **CollatingOrder** correspond à l’argument de paramètres régionaux de la méthode **CreateDatabase** lors de la création de la base de données ou à la méthode **CompactDatabase** lors du dernier compactage de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6aa62-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="6aa62-p102">Les paramètres de propriété **CollatingOrder** et **Attributes** d'un objet **Field2** d'une collection **Fields** d'un objet **Index** déterminent ensemble la séquence et la direction de l'ordre de tri dans un index. Toutefois, vous ne pouvez définir aucun ordre de tri pour un index individuel, vous pouvez uniquement le faire pour une table entière.</span><span class="sxs-lookup"><span data-stu-id="6aa62-p102">The **CollatingOrder** and **Attributes** property settings of a **Field2** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

