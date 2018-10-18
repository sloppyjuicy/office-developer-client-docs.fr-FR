---
title: Name, propriété (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90a77ae9d8c32ff8d0a13eacb146fc0e3ab3f397
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602467"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="2714b-102">Name, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2714b-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="2714b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2714b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2714b-104">Indique le nom d'un objet.</span><span class="sxs-lookup"><span data-stu-id="2714b-104">Indicates the name of an object.</span></span>

<span data-ttu-id="2714b-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="2714b-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="2714b-106">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="2714b-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="2714b-107">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="2714b-107">Return values</span></span>
>>>>>>> <span data-ttu-id="2714b-108">master</span><span class="sxs-lookup"><span data-stu-id="2714b-108">master</span></span>

<span data-ttu-id="2714b-109">Retourne une valeur de type **String** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2714b-109">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="2714b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2714b-110">Remarks</span></span>

<span data-ttu-id="2714b-p101">Vous pouvez récupérer la propriété **Name** d'un objet par référence ordinale, après quoi vous pouvez directement faire référence à l'objet par son nom. Si, par exemple, cdf.CubeDefs(0).Name produit la valeur « Bobs Video Store », vous pouvez faire référence à cet objet [CubeDef](cubedef-object-ado-md.md) comme suit : cdf.CubeDefs(« Bobs Video Store »).</span><span class="sxs-lookup"><span data-stu-id="2714b-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

