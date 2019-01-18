---
title: Propriété Fields.Count (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99eb21ba4f4ef13c902fc0d029dba59c30066853
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701192"
---
# <a name="fieldscount-property-dao"></a><span data-ttu-id="079af-102">Propriété Fields.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="079af-102">Fields.Count property (DAO)</span></span>


<span data-ttu-id="079af-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="079af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="079af-p101">Renvoie le nombre d'objets dans la collection spécifiée. Valeur **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="079af-p101">Returns the number of objects in the specified collection. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="079af-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="079af-106">Syntax</span></span>

<span data-ttu-id="079af-107">*expression* . Nombre</span><span class="sxs-lookup"><span data-stu-id="079af-107">*expression* .Count</span></span>

<span data-ttu-id="079af-108">*expression* Variable qui représente un objet **Fields** .</span><span class="sxs-lookup"><span data-stu-id="079af-108">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="079af-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="079af-109">Remarks</span></span>

<span data-ttu-id="079af-p102">Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="079af-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="079af-p103">La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="079af-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

