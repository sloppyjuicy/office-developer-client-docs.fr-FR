---
title: Errors. Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2cbbed2c7061b225d969dbd7554191e8db4a28a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293398"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="b1eb6-102">Errors. Count, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="b1eb6-102">Errors.Count property (DAO)</span></span>


<span data-ttu-id="b1eb6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1eb6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1eb6-104">Renvoie le nombre d'objets de la collection spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b1eb6-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="b1eb6-105">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b1eb6-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1eb6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1eb6-106">Syntax</span></span>

<span data-ttu-id="b1eb6-107">*expression* . Compte</span><span class="sxs-lookup"><span data-stu-id="b1eb6-107">*expression* .Count</span></span>

<span data-ttu-id="b1eb6-108">*expression* Variable qui représente un objet **Errors** .</span><span class="sxs-lookup"><span data-stu-id="b1eb6-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1eb6-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="b1eb6-109">Remarks</span></span>

<span data-ttu-id="b1eb6-p102">Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.</span><span class="sxs-lookup"><span data-stu-id="b1eb6-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="b1eb6-p103">Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="b1eb6-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

