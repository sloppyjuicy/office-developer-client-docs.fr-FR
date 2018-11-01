---
title: QueryDefs.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0092d3ad717b0f671273ca150698de005e7fe27f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881124"
---
# <a name="querydefscount-property-dao"></a><span data-ttu-id="4f329-102">QueryDefs.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="4f329-102">QueryDefs.Count Property (DAO)</span></span>


<span data-ttu-id="4f329-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f329-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f329-p101">Renvoie le nombre d'objets dans la collection spécifiée. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4f329-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f329-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f329-106">Syntax</span></span>

<span data-ttu-id="4f329-107">*expression* . Nombre</span><span class="sxs-lookup"><span data-stu-id="4f329-107">*expression* .Count</span></span>

<span data-ttu-id="4f329-108">*expression* Variable qui représente un objet **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="4f329-108">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f329-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="4f329-109">Remarks</span></span>

<span data-ttu-id="4f329-p102">Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="4f329-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="4f329-p103">La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="4f329-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

