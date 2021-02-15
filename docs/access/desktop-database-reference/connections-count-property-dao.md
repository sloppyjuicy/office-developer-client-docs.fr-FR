---
title: Connections.Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a286bf992116dc4ddfa71a9be8231e70b717aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295757"
---
# <a name="connectionscount-property-dao"></a><span data-ttu-id="050db-102">Connections.Count, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="050db-102">Connections.Count property (DAO)</span></span>


<span data-ttu-id="050db-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="050db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="050db-104">Renvoie le nombre d'objets **[Connection](connection-object-dao.md)** dans la collection **[Connections](connections-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="050db-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="050db-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="050db-105">Syntax</span></span>

<span data-ttu-id="050db-106">*.* Count</span><span class="sxs-lookup"><span data-stu-id="050db-106">*expression* .Count</span></span>

<span data-ttu-id="050db-107">*expression* Variable qui représente un **objet Connections.**</span><span class="sxs-lookup"><span data-stu-id="050db-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="050db-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="050db-108">Remarks</span></span>

<span data-ttu-id="050db-p101">Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.</span><span class="sxs-lookup"><span data-stu-id="050db-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="050db-p102">Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="050db-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

