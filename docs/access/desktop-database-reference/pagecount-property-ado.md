---
title: PageCount, propriété (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b37ccc0c9a61e00b3c2e8f5eb3367831e5ddea43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288118"
---
# <a name="pagecount-property-ado"></a><span data-ttu-id="56c9b-102">PageCount, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="56c9b-102">PageCount property (ADO)</span></span>


<span data-ttu-id="56c9b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56c9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56c9b-104">Indique le nombre de pages de données que contient l'objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="56c9b-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="56c9b-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="56c9b-105">Return value</span></span>

<span data-ttu-id="56c9b-106">Retourne une valeur de type **Long** qui indique le nombre de pages dans le **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="56c9b-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c9b-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="56c9b-107">Remarks</span></span>

<span data-ttu-id="56c9b-p101">Utilisez la propriété **PageCount** pour déterminer le nombre de pages que contient l’objet **Recordset**. Les *Pages* sont des groupes d’enregistrements dont la taille est égale à la valeur de la propriété [PageSize](pagesize-property-ado.md). Même si la dernière page est incomplète et que le nombre d’enregistrements qu’elle contient est inférieur à la valeur de **PageSize**, elle est considérée comme une page supplémentaire dans la valeur **PageCount**. Si l’objet **Recordset** ne prend pas en charge cette propriété, la valeur sera -1, pour indiquer que la propriété **PageCount** ne peut pas être déterminée.</span><span class="sxs-lookup"><span data-stu-id="56c9b-p101">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object. *Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting. Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="56c9b-112">Pour plus d'informations sur les fonctionnalités relatives aux pages, voir les propriétés **PageSize** et [AbsolutePage](absolutepage-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="56c9b-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

