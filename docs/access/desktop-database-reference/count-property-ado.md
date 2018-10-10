---
title: Count, propriété (ADO)
TOCTitle: Count Property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad02d854a560e3fa99bf7454c97083e88638c520
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470693"
---
# <a name="count-property-ado"></a><span data-ttu-id="8ed9a-102">Count, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ed9a-102">Count Property (ADO)</span></span>


<span data-ttu-id="8ed9a-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ed9a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8ed9a-104">Indique le nombre d'objets d'une collection.</span><span class="sxs-lookup"><span data-stu-id="8ed9a-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ed9a-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8ed9a-105">Return Value</span></span>

<span data-ttu-id="8ed9a-106">Renvoie une valeur de type **Long**</span><span class="sxs-lookup"><span data-stu-id="8ed9a-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed9a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8ed9a-107">Remarks</span></span>

<span data-ttu-id="8ed9a-108">Utilisez la propriété **Count** pour déterminer le nombre d'objets figurant dans une collection déterminée.</span><span class="sxs-lookup"><span data-stu-id="8ed9a-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="8ed9a-p101">Dans la mesure où la numérotation des membres d'une collection commence par 0, vous devez toujours coder les boucles en commençant par le membre 0 et finir par la valeur de la propriété **Count** moins 1. Si vous utilisez Microsoft Visual Basic et que vous souhaitez parcourir les membres d'une collection sans vérifier la propriété **Count**, utilisez la commande **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="8ed9a-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="8ed9a-111">Si la propriété **Count** a la valeur 0, il n'y a pas d'objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8ed9a-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

