---
title: Propriété Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95c2776e04497a1ac7f645659c7acc5d9eee2a63
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715962"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="dd121-102">Propriété Field.OriginalValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="dd121-102">Field.OriginalValue property (DAO)</span></span>


<span data-ttu-id="dd121-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd121-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="dd121-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd121-104">Syntax</span></span>

<span data-ttu-id="dd121-105">*expression* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="dd121-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="dd121-106">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="dd121-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd121-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd121-107">Remarks</span></span>

<span data-ttu-id="dd121-p101">Lors d'une mise à jour en lot optimiste, une collision peut survenir dans le cas où un second client modifie le même champ et le même enregistrement entre le moment où le premier client extrait les données et celui où il essaie de les mettre à jour. La propriété **OriginalValue** renferme la valeur du champ au moment du lancement de la dernière opération **Update** en lot. Si cette valeur ne correspond pas à celle de la base de données lorsque la méthode **Update** en lot tente d'écrire dans la base de données, une collision survient. Dans ce cas, la nouvelle valeur de la base de données est accessible via la propriété **[VisibleValue](field-visiblevalue-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="dd121-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

