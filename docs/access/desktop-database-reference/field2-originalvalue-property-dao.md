---
title: Field2.OriginalValue, propriété (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292740"
---
# <a name="field2originalvalue-property-dao"></a><span data-ttu-id="8028c-102">Field2.OriginalValue, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="8028c-102">Field2.OriginalValue property (DAO)</span></span>


<span data-ttu-id="8028c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8028c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8028c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8028c-104">Syntax</span></span>

<span data-ttu-id="8028c-105">*.* OriginalValue</span><span class="sxs-lookup"><span data-stu-id="8028c-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="8028c-106">*expression* une variable qui représente une **champ2** objet.</span><span class="sxs-lookup"><span data-stu-id="8028c-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8028c-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="8028c-107">Remarks</span></span>

<span data-ttu-id="8028c-p101">Lors d'une mise à jour en lot optimiste, une collision peut survenir dans le cas où un second client modifie le même champ et le même enregistrement entre le moment où le premier client extrait les données et celui où il essaie de les mettre à jour. La propriété **OriginalValue** renferme la valeur du champ au moment du lancement de la dernière opération **Update** en lot. Si cette valeur ne correspond pas à celle de la base de données lorsque la méthode **Update** en lot tente d'écrire dans la base de données, une collision survient. Dans ce cas, la nouvelle valeur de la base de données est accessible via la propriété **VisibleValue**.</span><span class="sxs-lookup"><span data-stu-id="8028c-p101">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt. The **OriginalValue** property contains the value of the field at the time the last batch **Update** began. If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs. When this happens, the new value in the database will be accessible through the **VisibleValue** property.</span></span>

