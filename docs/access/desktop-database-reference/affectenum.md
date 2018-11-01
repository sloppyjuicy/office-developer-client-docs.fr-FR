---
title: AffectEnum (référence de base de données du bureau Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9725a0e4af6ac6d25140739d6604abae6b76dcb6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879444"
---
# <a name="affectenum"></a><span data-ttu-id="fe405-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="fe405-102">AffectEnum</span></span>

<span data-ttu-id="fe405-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe405-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe405-104">Indique les enregistrements affectés par une opération.</span><span class="sxs-lookup"><span data-stu-id="fe405-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe405-105">Constante</span><span class="sxs-lookup"><span data-stu-id="fe405-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fe405-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe405-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fe405-107">Description</span><span class="sxs-lookup"><span data-stu-id="fe405-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe405-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="fe405-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="fe405-109">3</span><span class="sxs-lookup"><span data-stu-id="fe405-109">3</span></span></p></td>
<td><p><span data-ttu-id="fe405-110">Si aucun <a href="filter-property-ado.md">filtre</a> n’est appliqué au <strong>Recordset</strong>, affecte tous les enregistrements.
</span><span class="sxs-lookup"><span data-stu-id="fe405-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="fe405-111">Si la propriété <strong>Filter</strong> définit un critère de chaîne (tel que &quot;auteur = 'Martin'&quot;), l’opération affecte les enregistrements visibles dans le chapitre actif.</span><span class="sxs-lookup"><span data-stu-id="fe405-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="fe405-112">Si la propriété <strong>Filter</strong> définit un membre de <a href="filtergroupenum.md">FilterGroupEnum</a> ou un tableau de signets, l’opération affectera toutes les lignes du <strong>jeu d’enregistrements</strong>.</span><span class="sxs-lookup"><span data-stu-id="fe405-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p>
<p><span data-ttu-id="fe405-113"><strong>Remarque</strong>: adAffectAll est caché dans l’Explorateur d’objets Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fe405-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe405-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="fe405-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="fe405-115">4</span><span class="sxs-lookup"><span data-stu-id="fe405-115">4</span></span></p></td>
<td><p><span data-ttu-id="fe405-116">Affecte tous les enregistrements de tous les chapitres de même niveau du <strong>Recordset</strong>, notamment ceux non visibles par le <strong>filtre</strong> appliqué.</span><span class="sxs-lookup"><span data-stu-id="fe405-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe405-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="fe405-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="fe405-118">1</span><span class="sxs-lookup"><span data-stu-id="fe405-118">1</span></span></p></td>
<td><p><span data-ttu-id="fe405-119">N'affecte que l'enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="fe405-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe405-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="fe405-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="fe405-121">2</span><span class="sxs-lookup"><span data-stu-id="fe405-121">2</span></span></p></td>
<td><p><span data-ttu-id="fe405-p102">N’affecte que les enregistrements qui répondent aux paramètres de la propriété <a href="filter-property-ado.md">Filter</a> en cours. Pour utiliser cette option, vous devez configurer la propriété <strong>Filter</strong> avec la valeur <strong>FilterGroupEnum</strong> ou un tableau <strong>Bookmarks</strong>.</span><span class="sxs-lookup"><span data-stu-id="fe405-p102">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting. You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="fe405-124">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="fe405-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="fe405-125">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fe405-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe405-126">Constante</span><span class="sxs-lookup"><span data-stu-id="fe405-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe405-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="fe405-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe405-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="fe405-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe405-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="fe405-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe405-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="fe405-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

