---
title: Relations.Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: 7cb3885f-6896-8402-8b18-12769473f051
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196377(v=office.15)
ms:contentKeyID: 48545843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dd9cc00d2dc33263d6226783770fdae5207137f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306957"
---
# <a name="relationscount-property-dao"></a><span data-ttu-id="f0945-102">Relations.Count, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="f0945-102">Relations.Count property (DAO)</span></span>


<span data-ttu-id="f0945-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0945-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0945-104">Renvoie le nombre d'objets de la collection spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f0945-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="f0945-105">En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f0945-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0945-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0945-106">Syntax</span></span>

<span data-ttu-id="f0945-107">*.* Count</span><span class="sxs-lookup"><span data-stu-id="f0945-107">*expression* .Count</span></span>

<span data-ttu-id="f0945-108">*expression* Variable qui représente un objet **Relations.**</span><span class="sxs-lookup"><span data-stu-id="f0945-108">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0945-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0945-109">Remarks</span></span>

<span data-ttu-id="f0945-p102">Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.</span><span class="sxs-lookup"><span data-stu-id="f0945-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="f0945-p103">Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="f0945-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

