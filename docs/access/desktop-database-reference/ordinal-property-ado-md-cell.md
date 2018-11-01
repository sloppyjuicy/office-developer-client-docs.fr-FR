---
title: Ordinal, propriété (Cellule ADO MD)
TOCTitle: Ordinal Property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa85626b0de3a907d5a7ebf79cf333f76f42426e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867978"
---
# <a name="ordinal-property-ado-md-cell"></a><span data-ttu-id="e8cc6-102">Ordinal, propriété (Cellule ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e8cc6-102">Ordinal Property (ADO MD Cell)</span></span>


<span data-ttu-id="e8cc6-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8cc6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8cc6-104">Identifie de manière unique une cellule au sein d'un ensemble de cellules.</span><span class="sxs-lookup"><span data-stu-id="e8cc6-104">Uniquely identifies a cell by its position within a cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="e8cc6-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e8cc6-105">Return values</span></span>

<span data-ttu-id="e8cc6-106">Renvoie un nombre entier de type **Long** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e8cc6-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8cc6-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8cc6-107">Remarks</span></span>

<span data-ttu-id="e8cc6-p101">La valeur ordinale d’une cellule identifie de manière unique la cellule au sein d’un ensemble. En théorie, les cellules sont numérotées dans un ensemble de cellules comme si ce dernier était un tableau *p*-dimensionnel, où *p* correspond au nombre des [axes](axes-collection-ado-md.md). Les cellules sont numérotées à partir de zéro en ordre ligne-majeur.</span><span class="sxs-lookup"><span data-stu-id="e8cc6-p101">The cell's ordinal value uniquely identifies the cell within a cellset. Conceptually, cells are numbered in a cellset as if the cellset were a *p*-dimensional array, where *p* is the number of [axes](axes-collection-ado-md.md). Cells are numbered starting from zero in row-major order.</span></span>

<span data-ttu-id="e8cc6-111">Utilisée avec la propriété [Item](item-property-ado-md-cellset.md) de l'objet [Cellset](cellset-object-ado-md.md), la valeur ordinale de la cellule permet d'extraire rapidement la [cellule](cell-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="e8cc6-111">The cell's ordinal value can be used with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object to quickly retrieve the [Cell](cell-object-ado-md.md).</span></span>

