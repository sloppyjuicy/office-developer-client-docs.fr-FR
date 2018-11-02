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
ms.openlocfilehash: b01ec200278095893214f10dc9e50c5266153d72
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918932"
---
# <a name="documentscount-property-dao"></a><span data-ttu-id="864cb-102">Propriété Documents.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="864cb-102">Documents.Count property (DAO)</span></span>


<span data-ttu-id="864cb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="864cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="864cb-p101">Renvoie le nombre d'objets dans la collection spécifiée. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="864cb-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="864cb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="864cb-106">Syntax</span></span>

<span data-ttu-id="864cb-107">*expression* . Nombre</span><span class="sxs-lookup"><span data-stu-id="864cb-107">*expression* .Count</span></span>

<span data-ttu-id="864cb-108">*expression* Variable qui représente un objet **Documents** .</span><span class="sxs-lookup"><span data-stu-id="864cb-108">*expression* A variable that represents a **Documents** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="864cb-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="864cb-109">Remarks</span></span>

<span data-ttu-id="864cb-p102">Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="864cb-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="864cb-p103">La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="864cb-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

