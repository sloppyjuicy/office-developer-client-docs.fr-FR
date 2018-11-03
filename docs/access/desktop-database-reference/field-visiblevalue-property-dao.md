---
title: Propriété Field.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 461b8c43bf9000e5ecde3a3676cebf54be8e4166
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927570"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="57a37-102">Propriété Field.VisibleValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="57a37-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="57a37-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57a37-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="57a37-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57a37-104">Syntax</span></span>

<span data-ttu-id="57a37-105">*expression* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="57a37-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="57a37-106">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="57a37-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="57a37-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="57a37-107">Remarks</span></span>

<span data-ttu-id="57a37-p101">Cette propriété contient la valeur du champ se trouvant actuellement dans la base de données sur le serveur. Pendant une mise à jour par lot optimiste, une collision peut se produire, si un deuxième client a modifié le même champ et enregistrement entre le moment où le premier client a récupéré les données et la première tentative de mise à jour par le premier client. Lorsque cela se produit, la valeur définie par le deuxième client est accessible grâce à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="57a37-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

