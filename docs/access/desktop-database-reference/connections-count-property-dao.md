---
title: Propriété Connections.Count (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 572fed8afa9eb0f40a2b4938a31e866824147c83
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924468"
---
# <a name="connectionscount-property-dao"></a><span data-ttu-id="9b830-102">Propriété Connections.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b830-102">Connections.Count property (DAO)</span></span>


<span data-ttu-id="9b830-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b830-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b830-104">Renvoie le nombre d'objets **[Connection](connection-object-dao.md)** dans la collection **[Connections](connections-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9b830-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b830-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b830-105">Syntax</span></span>

<span data-ttu-id="9b830-106">*expression* . Nombre</span><span class="sxs-lookup"><span data-stu-id="9b830-106">*expression* .Count</span></span>

<span data-ttu-id="9b830-107">*expression* Variable qui représente un objet **Connections** .</span><span class="sxs-lookup"><span data-stu-id="9b830-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b830-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="9b830-108">Remarks</span></span>

<span data-ttu-id="9b830-p101">Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="9b830-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="9b830-p102">La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="9b830-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

