---
title: Axis, objet (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23fdb0d9ba636ae58fa19b42d5a8a47cb01d4ab2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720729"
---
# <a name="axis-object-ado-md"></a><span data-ttu-id="94a30-102">Axis, objet (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="94a30-102">Axis object (ADO MD)</span></span>


<span data-ttu-id="94a30-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94a30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94a30-104">Représente un axe de position ou de filtrage d'un ensemble de cellules, contenant des membres sélectionnés d'une ou plusieurs dimensions.</span><span class="sxs-lookup"><span data-stu-id="94a30-104">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="94a30-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="94a30-105">Remarks</span></span>

<span data-ttu-id="94a30-106">Un objet **Axis** peut faire partie d'une collection [Axes](axes-collection-ado-md.md) ou être renvoyé par la propriété [FilterAxis](filteraxis-property-ado-md.md) d'un [ensemble de cellules](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="94a30-106">An **Axis** object can be contained by an [Axes](axes-collection-ado-md.md) collection, or returned by the [FilterAxis](filteraxis-property-ado-md.md) property of a [Cellset](cellset-object-ado-md.md).</span></span>

<span data-ttu-id="94a30-107">Avec les collections et propriétés d'un objet **Axis**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="94a30-107">With the collections and properties of an **Axis** object, you can do the following:</span></span>

- <span data-ttu-id="94a30-108">Identifier l' **axe** à l'aide de la propriété [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="94a30-108">Identify the **Axis** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="94a30-109">Parcourir chaque position le long d'un **axe** à l'aide de la collection [Positions](positions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="94a30-109">Iterate through each position along an **Axis** using the [Positions](positions-collection-ado-md.md) collection.</span></span>

- <span data-ttu-id="94a30-110">Obtenir le nombre de dimensions sur l' **axe** à l'aide de la propriété [DimensionCount](dimensioncount-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="94a30-110">Obtain the number of dimensions on the **Axis** with the [DimensionCount](dimensioncount-property-ado-md.md) property.</span></span>

- <span data-ttu-id="94a30-111">Obtenir les attributs spécifiques au fournisseur de l' **axe** à l'aide de la collection ADO standard [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="94a30-111">Obtain provider-specific attributes of the **Axis** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

