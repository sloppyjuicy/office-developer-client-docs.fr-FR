---
title: Propriété QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0c1a85029270641a944d822ee81954ca1f2528e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919807"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="2b208-102">Propriété QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="2b208-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="2b208-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b208-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b208-p101">Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2b208-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b208-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b208-106">Syntax</span></span>

<span data-ttu-id="2b208-107">*expression* . Mise à jour</span><span class="sxs-lookup"><span data-stu-id="2b208-107">*expression* .Updatable</span></span>

<span data-ttu-id="2b208-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="2b208-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b208-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="2b208-109">Remarks</span></span>

<span data-ttu-id="2b208-110">La propriété **Updatable** d'un objet **QueryDef** a la valeur **True** si la définition de la requête peut être mise à jour même si l'objet **[Recordset](recordset-object-dao.md)** résultat n'est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="2b208-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

