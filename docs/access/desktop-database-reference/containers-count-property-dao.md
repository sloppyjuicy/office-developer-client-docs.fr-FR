---
title: Containers. Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7553b0e7d64e059dfeed50f158f21f48455976d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295589"
---
# <a name="containerscount-property-dao"></a><span data-ttu-id="5d473-102">Containers. Count, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="5d473-102">Containers.Count property (DAO)</span></span>


<span data-ttu-id="5d473-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d473-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d473-104">Renvoie le nombre d'objets **[Connection](connection-object-dao.md)** dans la collection **[Connections](connections-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="5d473-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d473-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d473-105">Syntax</span></span>

<span data-ttu-id="5d473-106">*expression* . Compte</span><span class="sxs-lookup"><span data-stu-id="5d473-106">*expression* .Count</span></span>

<span data-ttu-id="5d473-107">*expression* Variable qui représente un objet **connections** .</span><span class="sxs-lookup"><span data-stu-id="5d473-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d473-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d473-108">Remarks</span></span>

<span data-ttu-id="5d473-p101">Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.</span><span class="sxs-lookup"><span data-stu-id="5d473-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="5d473-p102">Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="5d473-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

