---
title: ObjectTypeEnum (référence de base de données de bureau Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288531"
---
# <a name="objecttypeenum"></a><span data-ttu-id="28271-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="28271-102">ObjectTypeEnum</span></span>

<span data-ttu-id="28271-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28271-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28271-104">Indique le type d'objet de base de données dont il faut définir les autorisations ou le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="28271-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28271-105">Constante</span><span class="sxs-lookup"><span data-stu-id="28271-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="28271-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="28271-106">Value</span></span></p></th>
<th><p><span data-ttu-id="28271-107">Description</span><span class="sxs-lookup"><span data-stu-id="28271-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28271-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="28271-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="28271-109">n°2</span><span class="sxs-lookup"><span data-stu-id="28271-109">2</span></span></p></td>
<td><p><span data-ttu-id="28271-110">L'objet est une colonne.</span><span class="sxs-lookup"><span data-stu-id="28271-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28271-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="28271-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="28271-112">3</span><span class="sxs-lookup"><span data-stu-id="28271-112">3</span></span></p></td>
<td><p><span data-ttu-id="28271-113">L'objet est une base de données.</span><span class="sxs-lookup"><span data-stu-id="28271-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28271-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="28271-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="28271-115">4</span><span class="sxs-lookup"><span data-stu-id="28271-115">4</span></span></p></td>
<td><p><span data-ttu-id="28271-116">L'objet est une procédure.</span><span class="sxs-lookup"><span data-stu-id="28271-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28271-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="28271-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="28271-118">-1</span><span class="sxs-lookup"><span data-stu-id="28271-118">-1</span></span></p></td>
<td><p><span data-ttu-id="28271-p101">L’objet est un type défini par le fournisseur. Une erreur se produit lorsque le paramètre <em>TypeObjet</em> a la valeur <strong>adPermObjProviderSpecific</strong> et que le paramètre<em>IdTypeObjet</em> n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="28271-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28271-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="28271-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="28271-122">0,1</span><span class="sxs-lookup"><span data-stu-id="28271-122">1</span></span></p></td>
<td><p><span data-ttu-id="28271-123">L'objet est une table.</span><span class="sxs-lookup"><span data-stu-id="28271-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28271-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="28271-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="28271-125">disque</span><span class="sxs-lookup"><span data-stu-id="28271-125">5</span></span></p></td>
<td><p><span data-ttu-id="28271-126">L'objet est une vue.</span><span class="sxs-lookup"><span data-stu-id="28271-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

