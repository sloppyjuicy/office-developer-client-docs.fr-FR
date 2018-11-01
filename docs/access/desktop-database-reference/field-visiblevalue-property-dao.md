---
title: Field.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 462359ca02b4a5724c781da303b13a97c73be388
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871205"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="9ebb7-102">Field.VisibleValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ebb7-102">Field.VisibleValue Property (DAO)</span></span>


<span data-ttu-id="9ebb7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ebb7-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebb7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ebb7-104">Syntax</span></span>

<span data-ttu-id="9ebb7-105">*expression* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="9ebb7-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="9ebb7-106">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="9ebb7-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ebb7-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ebb7-107">Remarks</span></span>

<span data-ttu-id="9ebb7-p101">Cette propriété contient la valeur du champ se trouvant actuellement dans la base de données sur le serveur. Pendant une mise à jour par lot optimiste, une collision peut se produire, si un deuxième client a modifié le même champ et enregistrement entre le moment où le premier client a récupéré les données et la première tentative de mise à jour par le premier client. Lorsque cela se produit, la valeur définie par le deuxième client est accessible grâce à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

