---
title: QueryDef.Updatable, propriété (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303331"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="7b053-102">QueryDef.Updatable, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="7b053-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="7b053-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b053-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b053-p101">Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Type de données **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7b053-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b053-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b053-106">Syntax</span></span>

<span data-ttu-id="7b053-107">*.* Updatable</span><span class="sxs-lookup"><span data-stu-id="7b053-107">*expression* .Updatable</span></span>

<span data-ttu-id="7b053-108">*expression* Variable représentant un objet **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="7b053-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b053-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b053-109">Remarks</span></span>

<span data-ttu-id="7b053-110">La propriété **Updatable** d'un objet **QueryDef** a la valeur **True** si la définition de la requête peut être mise à jour même si l'objet **[Recordset](recordset-object-dao.md)** résultat n'est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="7b053-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

