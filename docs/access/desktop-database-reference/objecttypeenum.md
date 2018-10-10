---
title: ObjectTypeEnum (référence de base de données du bureau Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38992451063e71609ab822bb231362f7a0f2cb3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469613"
---
# <a name="objecttypeenum"></a><span data-ttu-id="e9d27-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="e9d27-102">ObjectTypeEnum</span></span>


<span data-ttu-id="e9d27-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9d27-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e9d27-104">Indique le type d'objet de base de données dont il faut définir les autorisations ou le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e9d27-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9d27-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e9d27-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e9d27-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9d27-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e9d27-107">Description</span><span class="sxs-lookup"><span data-stu-id="e9d27-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9d27-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="e9d27-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="e9d27-109">2</span><span class="sxs-lookup"><span data-stu-id="e9d27-109">2</span></span></p></td>
<td><p><span data-ttu-id="e9d27-110">L'objet est une colonne.</span><span class="sxs-lookup"><span data-stu-id="e9d27-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9d27-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="e9d27-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="e9d27-112">3</span><span class="sxs-lookup"><span data-stu-id="e9d27-112">3</span></span></p></td>
<td><p><span data-ttu-id="e9d27-113">L'objet est une base de données.</span><span class="sxs-lookup"><span data-stu-id="e9d27-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9d27-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="e9d27-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="e9d27-115">4</span><span class="sxs-lookup"><span data-stu-id="e9d27-115">4</span></span></p></td>
<td><p><span data-ttu-id="e9d27-116">L'objet est une procédure.</span><span class="sxs-lookup"><span data-stu-id="e9d27-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9d27-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="e9d27-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="e9d27-118">-1</span><span class="sxs-lookup"><span data-stu-id="e9d27-118">-1</span></span></p></td>
<td><p><span data-ttu-id="e9d27-p101">L’objet est un type défini par le fournisseur. Une erreur se produit lorsque le paramètre <em>TypeObjet</em> a la valeur <strong>adPermObjProviderSpecific</strong> et que le paramètre<em>IdTypeObjet</em> n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="e9d27-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9d27-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="e9d27-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="e9d27-122">1</span><span class="sxs-lookup"><span data-stu-id="e9d27-122">1</span></span></p></td>
<td><p><span data-ttu-id="e9d27-123">L'objet est une table.</span><span class="sxs-lookup"><span data-stu-id="e9d27-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9d27-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="e9d27-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="e9d27-125">5</span><span class="sxs-lookup"><span data-stu-id="e9d27-125">5</span></span></p></td>
<td><p><span data-ttu-id="e9d27-126">L'objet est une vue.</span><span class="sxs-lookup"><span data-stu-id="e9d27-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

