---
title: FilterAxis, propriété (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713267"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="9a32c-102">FilterAxis, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="9a32c-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="9a32c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a32c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a32c-104">Fournit des informations de filtrage concernant l'ensemble de cellules actif.</span><span class="sxs-lookup"><span data-stu-id="9a32c-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="9a32c-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="9a32c-105">Return values</span></span>

<span data-ttu-id="9a32c-106">Retourne un objet [Axis](axis-object-ado-md.md) et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a32c-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a32c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9a32c-107">Remarks</span></span>

<span data-ttu-id="9a32c-p101">Utilisez la propriété **FilterAxis** pour retourner les informations sur les dimensions utilisées pour découper les données. La propriété [DimensionCount](dimensioncount-property-ado-md.md) de l'objet **Axis** retourne le nombre de dimensions de découpage. Cet axe comprend généralement une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="9a32c-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="9a32c-111">L'objet **Axis** retourné par [FilterAxis](filteraxis-property-ado-md.md) n'est pas compris dans la collection [Axes](axes-collection-ado-md.md) d'un objet [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="9a32c-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

