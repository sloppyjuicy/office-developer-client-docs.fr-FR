---
title: Delete, méthode (collection Fields ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fc2e614916026effe6ee0a9766e0b23db200574
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886395"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="38aa6-102">Delete, méthode (collection Fields ADO)</span><span class="sxs-lookup"><span data-stu-id="38aa6-102">Delete Method (ADO Fields Collection)</span></span>


<span data-ttu-id="38aa6-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38aa6-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="38aa6-104">Supprime un objet de la collection [Fields](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="38aa6-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="38aa6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38aa6-105">Syntax</span></span>

<span data-ttu-id="38aa6-106">*Champs*. Supprimer le*champ*</span><span class="sxs-lookup"><span data-stu-id="38aa6-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="38aa6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38aa6-107">Parameters</span></span>

  - <span data-ttu-id="38aa6-108">*Field*</span><span class="sxs-lookup"><span data-stu-id="38aa6-108">*Field*</span></span>

  - <span data-ttu-id="38aa6-109">**Variant** qui désigne l’objet [Field](field-object-ado.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="38aa6-109">A **Variant** that designates the [Field](field-object-ado.md) object to delete.</span></span> <span data-ttu-id="38aa6-110">Ce paramètre peut être le nom de l’objet **Field** ou la position ordinale de l’objet **Field** lui-même.</span><span class="sxs-lookup"><span data-stu-id="38aa6-110">This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>

## <a name="remarks"></a><span data-ttu-id="38aa6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="38aa6-111">Remarks</span></span>

<span data-ttu-id="38aa6-112">L'appel de la méthode **Fields.Delete** sur un objet [Recordset](recordset-object-ado.md) ouvert provoque un erreur d'exécution.</span><span class="sxs-lookup"><span data-stu-id="38aa6-112">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

