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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288657"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="21767-102">Name, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="21767-102">Name property (ADO MD)</span></span>


<span data-ttu-id="21767-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21767-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21767-104">Indique le nom d'un objet.</span><span class="sxs-lookup"><span data-stu-id="21767-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="21767-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="21767-105">Return values</span></span>

<span data-ttu-id="21767-106">Retourne une valeur de type **String** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="21767-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="21767-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="21767-107">Remarks</span></span>

<span data-ttu-id="21767-p101">Vous pouvez récupérer la propriété **Name** d’un objet par référence ordinale, après quoi vous pouvez directement faire référence à l’objet par son nom. Si, par exemple, cdf.CubeDefs(0).Name produit la valeur « Bobs Video Store », vous pouvez faire référence à cet objet [CubeDef](cubedef-object-ado-md.md) comme suit : cdf.CubeDefs(« Bobs Video Store »).</span><span class="sxs-lookup"><span data-stu-id="21767-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

