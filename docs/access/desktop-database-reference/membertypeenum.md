---
title: MemberTypeEnum (référence de base de données de bureau Access)
TOCTitle: MemberTypeEnum
ms:assetid: 3b6f9fff-fe54-b917-9404-927e3a627e0b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249150(v=office.15)
ms:contentKeyID: 48544286
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 82d507457d9242daa92cc0218c87bae4d82759a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289202"
---
# <a name="membertypeenum"></a><span data-ttu-id="5d3e0-102">MemberTypeEnum</span><span class="sxs-lookup"><span data-stu-id="5d3e0-102">MemberTypeEnum</span></span>

<span data-ttu-id="5d3e0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d3e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d3e0-104">Spécifie le paramétrage de la propriété [Type](type-property-ado-md.md) d’un objet [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="5d3e0-104">Specifies the setting for the [Type](type-property-ado-md.md) property of a [Member](member-object-ado-md.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d3e0-105">Constante</span><span class="sxs-lookup"><span data-stu-id="5d3e0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5d3e0-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d3e0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5d3e0-107">Description</span><span class="sxs-lookup"><span data-stu-id="5d3e0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d3e0-108"><strong>adMemberAll</strong></span><span class="sxs-lookup"><span data-stu-id="5d3e0-108"><strong>adMemberAll</strong></span></span></p></td>
<td><p><span data-ttu-id="5d3e0-109">4 </span><span class="sxs-lookup"><span data-stu-id="5d3e0-109">4</span></span></p></td>
<td><p><span data-ttu-id="5d3e0-110">Indique que l'objet <strong>Member</strong> représente tous les membres du niveau.</span><span class="sxs-lookup"><span data-stu-id="5d3e0-110">Indicates that the <strong>Member</strong> object represents all members of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d3e0-111"><strong>adMemberFormula</strong></span><span class="sxs-lookup"><span data-stu-id="5d3e0-111"><strong>adMemberFormula</strong></span></span></p></td>
<td><p><span data-ttu-id="5d3e0-112">3</span><span class="sxs-lookup"><span data-stu-id="5d3e0-112">3</span></span></p></td>
<td><p><span data-ttu-id="5d3e0-113">Indique que l'objet <strong>Member</strong> est calculé à l'aide d'une expression de formule.</span><span class="sxs-lookup"><span data-stu-id="5d3e0-113">Indicates that the <strong>Member</strong> object is calculated using a formula expression.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d3e0-114"><strong>adMemberMeasure</strong></span><span class="sxs-lookup"><span data-stu-id="5d3e0-114"><strong>adMemberMeasure</strong></span></span></p></td>
<td><p><span data-ttu-id="5d3e0-115">2</span><span class="sxs-lookup"><span data-stu-id="5d3e0-115">2</span></span></p></td>
<td><p><span data-ttu-id="5d3e0-116">Indique que l'objet <strong>Member</strong> appartient à la dimension Measures et représente un attribut quantitatif.</span><span class="sxs-lookup"><span data-stu-id="5d3e0-116">Indicates that the <strong>Member</strong> object belongs to the Measures dimension and represents a quantitative attribute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d3e0-117"><strong>adMemberRegular</strong></span><span class="sxs-lookup"><span data-stu-id="5d3e0-117"><strong>adMemberRegular</strong></span></span></p></td>
<td><p><span data-ttu-id="5d3e0-118">1</span><span class="sxs-lookup"><span data-stu-id="5d3e0-118">1</span></span></p></td>
<td><p><span data-ttu-id="5d3e0-p101">Valeur par défaut. Indique que l'objet <strong>Member</strong> représente une instance d'une entité métier.</span><span class="sxs-lookup"><span data-stu-id="5d3e0-p101">Default. Indicates that the <strong>Member</strong> object represents an instance of a business entity.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d3e0-121"><strong>adMemberUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="5d3e0-121"><strong>adMemberUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="5d3e0-122">0</span><span class="sxs-lookup"><span data-stu-id="5d3e0-122">0</span></span></p></td>
<td><p><span data-ttu-id="5d3e0-123">Il est impossible de déterminer le type du membre.</span><span class="sxs-lookup"><span data-stu-id="5d3e0-123">Cannot determine the type of the member.</span></span></p></td>
</tr>
</tbody>
</table>

