---
title: Name, propriété (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4e27870a0c1dbb38b7c0be31c439a95f6aae671
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704153"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="1f4fb-102">Name, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="1f4fb-102">Name property (ADO MD)</span></span>


<span data-ttu-id="1f4fb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f4fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f4fb-104">Indique le nom d'un objet.</span><span class="sxs-lookup"><span data-stu-id="1f4fb-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="1f4fb-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1f4fb-105">Return values</span></span>

<span data-ttu-id="1f4fb-106">Retourne une valeur de type **String** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1f4fb-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f4fb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1f4fb-107">Remarks</span></span>

<span data-ttu-id="1f4fb-p101">Vous pouvez récupérer la propriété **Name** d'un objet par référence ordinale, après quoi vous pouvez directement faire référence à l'objet par son nom. Si, par exemple, cdf.CubeDefs(0).Name produit la valeur « Bobs Video Store », vous pouvez faire référence à cet objet [CubeDef](cubedef-object-ado-md.md) comme suit : cdf.CubeDefs(« Bobs Video Store »).</span><span class="sxs-lookup"><span data-stu-id="1f4fb-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

