---
title: Propriété Fields.Count (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 317f98ec53b7b37664796d826fd6afc301b6b152
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930398"
---
# <a name="fieldscount-property-dao"></a><span data-ttu-id="954ae-102">Propriété Fields.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="954ae-102">Fields.Count property (DAO)</span></span>


<span data-ttu-id="954ae-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="954ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="954ae-p101">Renvoie le nombre d'objets dans la collection spécifiée. Valeur **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="954ae-p101">Returns the number of objects in the specified collection. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="954ae-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="954ae-106">Syntax</span></span>

<span data-ttu-id="954ae-107">*expression* . Nombre</span><span class="sxs-lookup"><span data-stu-id="954ae-107">*expression* .Count</span></span>

<span data-ttu-id="954ae-108">*expression* Variable qui représente un objet **Fields** .</span><span class="sxs-lookup"><span data-stu-id="954ae-108">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="954ae-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="954ae-109">Remarks</span></span>

<span data-ttu-id="954ae-p102">Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="954ae-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="954ae-p103">La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="954ae-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

