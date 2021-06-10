---
title: Documents.Count, propriété (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293741"
---
# <a name="documentscount-property-dao"></a><span data-ttu-id="80872-102">Documents.Count, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="80872-102">Documents.Count property (DAO)</span></span>


<span data-ttu-id="80872-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80872-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80872-p101">Renvoie le nombre d'objets de la collection spécifiée. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="80872-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80872-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80872-106">Syntax</span></span>

<span data-ttu-id="80872-107">*.* Count</span><span class="sxs-lookup"><span data-stu-id="80872-107">*expression* .Count</span></span>

<span data-ttu-id="80872-108">*expression* Variable qui représente un objet **Documents.**</span><span class="sxs-lookup"><span data-stu-id="80872-108">*expression* A variable that represents a **Documents** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="80872-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="80872-109">Remarks</span></span>

<span data-ttu-id="80872-p102">Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.</span><span class="sxs-lookup"><span data-stu-id="80872-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="80872-p103">Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="80872-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

