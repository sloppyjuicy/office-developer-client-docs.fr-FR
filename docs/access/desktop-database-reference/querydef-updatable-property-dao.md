---
title: QueryDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ad761c2941cb556ce67c9f716247663220f753f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873690"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="61b1c-102">QueryDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="61b1c-102">QueryDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="61b1c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61b1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61b1c-p101">Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="61b1c-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b1c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61b1c-106">Syntax</span></span>

<span data-ttu-id="61b1c-107">*expression* . Mise à jour</span><span class="sxs-lookup"><span data-stu-id="61b1c-107">*expression* .Updatable</span></span>

<span data-ttu-id="61b1c-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="61b1c-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="61b1c-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="61b1c-109">Remarks</span></span>

<span data-ttu-id="61b1c-110">La propriété **Updatable** d'un objet **QueryDef** a la valeur **True** si la définition de la requête peut être mise à jour même si l'objet **[Recordset](recordset-object-dao.md)** résultat n'est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="61b1c-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

