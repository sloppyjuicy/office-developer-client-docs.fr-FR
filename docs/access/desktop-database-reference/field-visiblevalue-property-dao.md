---
title: Field.VisibleValue, propriété (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292915"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="fa66a-102">Field.VisibleValue, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="fa66a-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="fa66a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa66a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="fa66a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa66a-104">Syntax</span></span>

<span data-ttu-id="fa66a-105">*.* VisibleValue</span><span class="sxs-lookup"><span data-stu-id="fa66a-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="fa66a-106">*expression* Variable qui représente un objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="fa66a-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa66a-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa66a-107">Remarks</span></span>

<span data-ttu-id="fa66a-p101">Cette propriété contient la valeur du champ actuellement dans la base de données sur le serveur. Lors d'une mise à jour en lot optimiste, une collision peut survenir dans le cas où un second client a modifié le même champ et le même enregistrement entre le moment où le premier client a extrait les données et celui où il essaie de les mettre à jour. Dans ce cas, la valeur définie par le second client est accessible via cette propriété.</span><span class="sxs-lookup"><span data-stu-id="fa66a-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

