---
title: Name, propriété (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 971a528c0efe97626f08ff94490e8aee25230f60
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926534"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="b83d6-102">Name, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="b83d6-102">Name property (ADO MD)</span></span>


<span data-ttu-id="b83d6-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b83d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b83d6-104">Indique le nom d'un objet.</span><span class="sxs-lookup"><span data-stu-id="b83d6-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="b83d6-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="b83d6-105">Return values</span></span>

<span data-ttu-id="b83d6-106">Retourne une valeur de type **String** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b83d6-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="b83d6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b83d6-107">Remarks</span></span>

<span data-ttu-id="b83d6-p101">Vous pouvez récupérer la propriété **Name** d'un objet par référence ordinale, après quoi vous pouvez directement faire référence à l'objet par son nom. Si, par exemple, cdf.CubeDefs(0).Name produit la valeur « Bobs Video Store », vous pouvez faire référence à cet objet [CubeDef](cubedef-object-ado-md.md) comme suit : cdf.CubeDefs(« Bobs Video Store »).</span><span class="sxs-lookup"><span data-stu-id="b83d6-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

