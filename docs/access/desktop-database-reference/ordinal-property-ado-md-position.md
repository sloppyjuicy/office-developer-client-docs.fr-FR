---
title: Ordinal, propriété (objet Position ADO MD)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e29b5c86e8f37d84116aa92432e93eb8943e29e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288189"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="a0d82-102">Ordinal, propriété (objet Position ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a0d82-102">Ordinal property (ADO MD Position)</span></span>


<span data-ttu-id="a0d82-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0d82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a0d82-104">Identifie de façon unique une position le long d'un axe.</span><span class="sxs-lookup"><span data-stu-id="a0d82-104">Uniquely identifies a position along an axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="a0d82-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a0d82-105">Return values</span></span>

<span data-ttu-id="a0d82-106">Retourne un entier de type **Long** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a0d82-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0d82-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="a0d82-107">Remarks</span></span>

<span data-ttu-id="a0d82-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span><span class="sxs-lookup"><span data-stu-id="a0d82-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="a0d82-109">Il est possible de récupérer rapidement une cellule en utilisant la propriété **Ordinal** de l'objet **Position** le long de chaque axe avec la propriété [Item](item-property-ado-md-cellset.md) de l'objet [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a0d82-109">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

