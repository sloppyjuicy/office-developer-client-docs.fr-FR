---
title: Field2.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9c901045f1f856142a628fb31806610e7d5dce43
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469470"
---
# <a name="field2visiblevalue-property-dao"></a><span data-ttu-id="6a5e5-102">Field2.VisibleValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6a5e5-102">Field2.VisibleValue Property (DAO)</span></span>


<span data-ttu-id="6a5e5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a5e5-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5e5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a5e5-104">Syntax</span></span>

<span data-ttu-id="6a5e5-105">*expression* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="6a5e5-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="6a5e5-106">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="6a5e5-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5e5-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="6a5e5-107">Remarks</span></span>

<span data-ttu-id="6a5e5-p101">Cette propriété contient la valeur du champ se trouvant actuellement dans la base de données sur le serveur. Pendant une mise à jour par lot optimiste, une collision peut se produire, si un deuxième client a modifié le même champ et enregistrement entre le moment où le premier client a récupéré les données et la première tentative de mise à jour par le premier client. Lorsque cela se produit, la valeur définie par le deuxième client est accessible grâce à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6a5e5-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

