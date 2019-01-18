---
title: Propriété Documents.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3fc0b1e6-f7be-cd43-711f-5cf5763fe7f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192858(v=office.15)
ms:contentKeyID: 48544407
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053325
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dd9cc563ecc885fca4fa0ef5829d82aa2f8bfef6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710684"
---
# <a name="documentscount-property-dao"></a><span data-ttu-id="28378-102">Propriété Documents.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="28378-102">Documents.Count property (DAO)</span></span>


<span data-ttu-id="28378-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28378-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28378-p101">Renvoie le nombre d'objets dans la collection spécifiée. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="28378-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="28378-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28378-106">Syntax</span></span>

<span data-ttu-id="28378-107">*expression* . Nombre</span><span class="sxs-lookup"><span data-stu-id="28378-107">*expression* .Count</span></span>

<span data-ttu-id="28378-108">*expression* Variable qui représente un objet **Documents** .</span><span class="sxs-lookup"><span data-stu-id="28378-108">*expression* A variable that represents a **Documents** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="28378-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="28378-109">Remarks</span></span>

<span data-ttu-id="28378-p102">Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="28378-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="28378-p103">La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="28378-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

