---
title: Propriété Databases.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd8908492721315202c5bdf26109753c88905a07
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720127"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="817c7-102">Propriété Databases.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="817c7-102">Databases.Count property (DAO)</span></span>


<span data-ttu-id="817c7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="817c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="817c7-p101">Renvoie le nombre d'objets dans la collection spécifiée. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="817c7-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="817c7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="817c7-106">Syntax</span></span>

<span data-ttu-id="817c7-107">*expression* . Nombre</span><span class="sxs-lookup"><span data-stu-id="817c7-107">*expression* .Count</span></span>

<span data-ttu-id="817c7-108">*expression* Variable qui représente un objet de **bases de données** .</span><span class="sxs-lookup"><span data-stu-id="817c7-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="817c7-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="817c7-109">Remarks</span></span>

<span data-ttu-id="817c7-p102">Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="817c7-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="817c7-p103">La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="817c7-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

