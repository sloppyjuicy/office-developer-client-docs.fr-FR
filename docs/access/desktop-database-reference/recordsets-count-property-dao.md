---
title: Recordsets.Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a81c1ede8a3afb95e39b2c33fb8112119faf8bd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309289"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="c0669-102">Recordsets.Count, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0669-102">Recordsets.Count property (DAO)</span></span>


<span data-ttu-id="c0669-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0669-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0669-104">Renvoie le nombre d'objets dans la collection spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c0669-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="c0669-105">Valeur **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0669-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0669-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0669-106">Syntax</span></span>

<span data-ttu-id="c0669-107">*.* Count</span><span class="sxs-lookup"><span data-stu-id="c0669-107">*expression* .Count</span></span>

<span data-ttu-id="c0669-108">*expression* Variable qui représente un objet **Recordsets.**</span><span class="sxs-lookup"><span data-stu-id="c0669-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0669-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0669-109">Remarks</span></span>

<span data-ttu-id="c0669-p102">Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.</span><span class="sxs-lookup"><span data-stu-id="c0669-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="c0669-p103">Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="c0669-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

