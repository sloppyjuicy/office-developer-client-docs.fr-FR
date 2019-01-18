---
title: Propriété QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713365"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="d2771-102">Propriété QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="d2771-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="d2771-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2771-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2771-p101">Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d2771-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2771-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2771-106">Syntax</span></span>

<span data-ttu-id="d2771-107">*expression* . Mise à jour</span><span class="sxs-lookup"><span data-stu-id="d2771-107">*expression* .Updatable</span></span>

<span data-ttu-id="d2771-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="d2771-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2771-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2771-109">Remarks</span></span>

<span data-ttu-id="d2771-110">La propriété **Updatable** d'un objet **QueryDef** a la valeur **True** si la définition de la requête peut être mise à jour même si l'objet **[Recordset](recordset-object-dao.md)** résultat n'est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="d2771-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

