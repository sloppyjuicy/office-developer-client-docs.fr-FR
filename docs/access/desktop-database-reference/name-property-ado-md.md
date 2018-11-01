---
title: Name, propriété (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63e098a8b97bb37fad2ef256affb2da142daf434
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878646"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="cc87d-102">Name, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="cc87d-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="cc87d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc87d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc87d-104">Indique le nom d'un objet.</span><span class="sxs-lookup"><span data-stu-id="cc87d-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="cc87d-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="cc87d-105">Return values</span></span>

<span data-ttu-id="cc87d-106">Retourne une valeur de type **String** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cc87d-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc87d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cc87d-107">Remarks</span></span>

<span data-ttu-id="cc87d-p101">Vous pouvez récupérer la propriété **Name** d'un objet par référence ordinale, après quoi vous pouvez directement faire référence à l'objet par son nom. Si, par exemple, cdf.CubeDefs(0).Name produit la valeur « Bobs Video Store », vous pouvez faire référence à cet objet [CubeDef](cubedef-object-ado-md.md) comme suit : cdf.CubeDefs(« Bobs Video Store »).</span><span class="sxs-lookup"><span data-stu-id="cc87d-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

