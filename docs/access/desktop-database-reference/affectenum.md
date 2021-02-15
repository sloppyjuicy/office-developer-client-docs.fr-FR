---
title: AffectEnum (référence de base de données de bureau Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297199"
---
# <a name="affectenum"></a><span data-ttu-id="78d3f-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="78d3f-102">AffectEnum</span></span>

<span data-ttu-id="78d3f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78d3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78d3f-104">Indique les enregistrements affectés par une opération.</span><span class="sxs-lookup"><span data-stu-id="78d3f-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78d3f-105">Constante</span><span class="sxs-lookup"><span data-stu-id="78d3f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="78d3f-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="78d3f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="78d3f-107">Description</span><span class="sxs-lookup"><span data-stu-id="78d3f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78d3f-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="78d3f-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="78d3f-109">3 </span><span class="sxs-lookup"><span data-stu-id="78d3f-109">3</span></span></p></td>
<td><p><span data-ttu-id="78d3f-110">Si aucun <a href="filter-property-ado.md">filtre</a> n’est appliqué au <strong>Recordset</strong>, affecte tous les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="78d3f-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="78d3f-111">Si la <strong>propriété Filter</strong> est définie sur un critère de chaîne (tel que &quot; Author='Smith' ), l’opération affecte les enregistrements &quot; visibles dans le chapitre actuel.</span><span class="sxs-lookup"><span data-stu-id="78d3f-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="78d3f-112">Si la <strong>propriété Filter</strong> est définie sur un membre du <a href="filtergroupenum.md">FilterGroupEnum</a> ou un tableau de signets, l’opération affectera toutes les lignes du jeu <strong>d’enregistrements</strong>.</span><span class="sxs-lookup"><span data-stu-id="78d3f-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="78d3f-113"><strong>REMARQUE</strong>: adAffectAll est masqué dans l’explorateur Visual Basic’objet.</span><span class="sxs-lookup"><span data-stu-id="78d3f-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78d3f-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="78d3f-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="78d3f-115">4 </span><span class="sxs-lookup"><span data-stu-id="78d3f-115">4</span></span></p></td>
<td><p><span data-ttu-id="78d3f-116">Affecte tous les enregistrements de tous les chapitres de même niveau du <strong>Recordset</strong>, notamment ceux non visibles par le <strong>filtre</strong> appliqué.</span><span class="sxs-lookup"><span data-stu-id="78d3f-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78d3f-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="78d3f-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="78d3f-118">1 </span><span class="sxs-lookup"><span data-stu-id="78d3f-118">1</span></span></p></td>
<td><p><span data-ttu-id="78d3f-119">N'affecte que l'enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="78d3f-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78d3f-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="78d3f-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="78d3f-121">2 </span><span class="sxs-lookup"><span data-stu-id="78d3f-121">2</span></span></p></td>
<td><p><span data-ttu-id="78d3f-p102">N’affecte que les enregistrements qui répondent aux paramètres de la propriété <a href="filter-property-ado.md">Filter</a> en cours. Pour utiliser cette option, vous devez configurer la propriété <strong>Filter</strong> avec la valeur <strong>FilterGroupEnum</strong> ou un tableau <strong>Bookmarks</strong>.</span><span class="sxs-lookup"><span data-stu-id="78d3f-p102">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting. You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="78d3f-124">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="78d3f-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="78d3f-125">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="78d3f-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78d3f-126">Constante</span><span class="sxs-lookup"><span data-stu-id="78d3f-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78d3f-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="78d3f-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78d3f-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="78d3f-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78d3f-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="78d3f-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78d3f-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="78d3f-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

