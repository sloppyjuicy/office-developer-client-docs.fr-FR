---
title: TableDefs.Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c997a437cc7a7ae1461e7308899c85dac44fbda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314265"
---
# <a name="tabledefscount-property-dao"></a><span data-ttu-id="037c3-102">TableDefs.Count, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="037c3-102">TableDefs.Count property (DAO)</span></span>


<span data-ttu-id="037c3-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="037c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="037c3-104">Renvoie le nombre d'objets de la collection spécifiée.</span><span class="sxs-lookup"><span data-stu-id="037c3-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="037c3-105">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="037c3-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="037c3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="037c3-106">Syntax</span></span>

<span data-ttu-id="037c3-107">*.* Count</span><span class="sxs-lookup"><span data-stu-id="037c3-107">*expression* .Count</span></span>

<span data-ttu-id="037c3-108">*expression* Variable qui représente un **objet TableDefs.**</span><span class="sxs-lookup"><span data-stu-id="037c3-108">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="037c3-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="037c3-109">Remarks</span></span>

<span data-ttu-id="037c3-p102">Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.</span><span class="sxs-lookup"><span data-stu-id="037c3-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="037c3-p103">Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="037c3-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

