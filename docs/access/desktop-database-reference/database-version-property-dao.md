---
title: Propriété Database.Version (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41b408f63522902fd1d4f806090eef7563a3492a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700067"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="f0387-102">Propriété Database.Version (DAO)</span><span class="sxs-lookup"><span data-stu-id="f0387-102">Database.Version property (DAO)</span></span>

<span data-ttu-id="f0387-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0387-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0387-p101">Dans un espace de travail Microsoft Access, renvoie la version du moteur de base de données Microsoft Jet ou Microsoft Access qui a créé la base de données. Valeur **String** en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0387-p101">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0387-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0387-106">Syntax</span></span>

<span data-ttu-id="f0387-107">*expression* . Version</span><span class="sxs-lookup"><span data-stu-id="f0387-107">*expression* .Version</span></span>

<span data-ttu-id="f0387-108">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="f0387-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0387-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0387-109">Remarks</span></span>

<span data-ttu-id="f0387-110">La valeur de retour est une chaîne (type de données String) qui est évaluée à un numéro de version et mise en forme comme suit.</span><span class="sxs-lookup"><span data-stu-id="f0387-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

- <span data-ttu-id="f0387-p102">Espace de travail Microsoft Access : numéro de version sous la forme « *version.inter* ». Par exemple, « 3.0 ». Le numéro de version du produit est constitué du numéro de version (3), d’un point et du numéro de version intermédiaire (0).</span><span class="sxs-lookup"><span data-stu-id="f0387-p102">Microsoft Access workspace represents the version number in the form "*major.minor*". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="f0387-114">Le tableau suivant montre la version du moteur de base de données incluse dans différentes versions de produits Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f0387-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0387-115">Moteur de base de données</span><span class="sxs-lookup"><span data-stu-id="f0387-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="f0387-116">Version (année de sortie)</span><span class="sxs-lookup"><span data-stu-id="f0387-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="f0387-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="f0387-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="f0387-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f0387-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="f0387-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="f0387-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="f0387-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="f0387-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0387-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="f0387-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="f0387-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="f0387-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="f0387-123">1.0</span><span class="sxs-lookup"><span data-stu-id="f0387-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="f0387-124">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="f0387-125">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="f0387-126">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0387-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="f0387-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="f0387-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="f0387-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="f0387-129">1.1</span><span class="sxs-lookup"><span data-stu-id="f0387-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="f0387-130">3.0</span><span class="sxs-lookup"><span data-stu-id="f0387-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="f0387-131">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="f0387-132">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0387-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="f0387-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="f0387-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="f0387-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="f0387-135">2.0</span><span class="sxs-lookup"><span data-stu-id="f0387-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="f0387-136">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="f0387-137">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="f0387-138">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0387-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="f0387-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="f0387-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="f0387-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="f0387-141">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="f0387-142">4.0 (16 bits)</span><span class="sxs-lookup"><span data-stu-id="f0387-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="f0387-143">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="f0387-144">S/O</span><span class="sxs-lookup"><span data-stu-id="f0387-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0387-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="f0387-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="f0387-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="f0387-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="f0387-147">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="f0387-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="f0387-148">4.0 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f0387-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="f0387-149">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="f0387-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="f0387-150">4.x</span><span class="sxs-lookup"><span data-stu-id="f0387-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0387-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="f0387-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="f0387-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="f0387-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="f0387-153">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="f0387-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="f0387-154">5.0</span><span class="sxs-lookup"><span data-stu-id="f0387-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="f0387-155">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="f0387-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="f0387-156">5.0</span><span class="sxs-lookup"><span data-stu-id="f0387-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0387-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="f0387-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="f0387-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="f0387-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="f0387-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="f0387-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f0387-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="f0387-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0387-161">Moteur de base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="f0387-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="f0387-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="f0387-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="f0387-163">2007</span><span class="sxs-lookup"><span data-stu-id="f0387-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

