---
title: Propriété Field2.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e3da5f7438ae83010c6ecc109dccf5d7a8eb9ef
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726133"
---
# <a name="field2originalvalue-property-dao"></a><span data-ttu-id="f3593-102">Propriété Field2.OriginalValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="f3593-102">Field2.OriginalValue property (DAO)</span></span>


<span data-ttu-id="f3593-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3593-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f3593-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3593-104">Syntax</span></span>

<span data-ttu-id="f3593-105">*expression* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="f3593-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="f3593-106">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="f3593-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3593-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3593-107">Remarks</span></span>

<span data-ttu-id="f3593-p101">Lors d'une mise à jour en lot optimiste, une collision peut survenir dans le cas où un second client modifie le même champ et le même enregistrement entre le moment où le premier client extrait les données et celui où il essaie de les mettre à jour. La propriété **OriginalValue** renferme la valeur du champ au moment du lancement de la dernière opération **Update** en lot. Si cette valeur ne correspond pas à celle de la base de données lorsque la méthode **Update** en lot tente d'écrire dans la base de données, une collision survient. Dans ce cas, la nouvelle valeur de la base de données est accessible via la propriété **VisibleValue**.</span><span class="sxs-lookup"><span data-stu-id="f3593-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **VisibleValue** property.</span></span>

