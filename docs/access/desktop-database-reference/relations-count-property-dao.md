---
title: Propriété Relations.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7cb3885f-6896-8402-8b18-12769473f051
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196377(v=office.15)
ms:contentKeyID: 48545843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5af98ffa550dc2ba959284e16af1e1bf5ac39328
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920738"
---
# <a name="relationscount-property-dao"></a><span data-ttu-id="71153-102">Propriété Relations.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="71153-102">Relations.Count property (DAO)</span></span>


<span data-ttu-id="71153-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71153-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71153-p101">Renvoie le nombre d'objets dans la collection spécifiée. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="71153-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71153-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71153-106">Syntax</span></span>

<span data-ttu-id="71153-107">*expression* . Nombre</span><span class="sxs-lookup"><span data-stu-id="71153-107">*expression* .Count</span></span>

<span data-ttu-id="71153-108">*expression* Variable qui représente un objet **Relations** .</span><span class="sxs-lookup"><span data-stu-id="71153-108">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="71153-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="71153-109">Remarks</span></span>

<span data-ttu-id="71153-p102">Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="71153-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="71153-p103">La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="71153-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

