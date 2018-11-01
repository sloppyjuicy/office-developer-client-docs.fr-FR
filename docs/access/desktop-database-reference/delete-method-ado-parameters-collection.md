---
title: Delete, méthode (collection Parameters ADO)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e519d40a081b132cd09030e9ba97de9e8987af99
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881957"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="1d7ed-102">Delete, méthode (collection Parameters ADO)</span><span class="sxs-lookup"><span data-stu-id="1d7ed-102">Delete Method (ADO Parameters Collection)</span></span>


<span data-ttu-id="1d7ed-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d7ed-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1d7ed-104">Supprime un objet de la collection [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1d7ed-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d7ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d7ed-105">Syntax</span></span>

<span data-ttu-id="1d7ed-106">*Paramètres*. Supprimer *l’Index*</span><span class="sxs-lookup"><span data-stu-id="1d7ed-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="1d7ed-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d7ed-107">Parameters</span></span>

  - <span data-ttu-id="1d7ed-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="1d7ed-108">*Index*</span></span>

  - <span data-ttu-id="1d7ed-109">Valeur de type **String** contenant le nom de l'objet que vous voulez supprimer ou la position ordinale (index) de l'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-109">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d7ed-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1d7ed-110">Remarks</span></span>

<span data-ttu-id="1d7ed-p101">L'utilisation de la méthode **Delete** sur une collection permet de supprimer l'un des objets figurant dans cette collection. Cette méthode est uniquement disponible pour la collection **Parameters** d'un objet [Command](command-object-ado.md). Vous devez utiliser la propriété [Name](parameter-object-ado.md) de l'objet [Parameter](name-property-ado.md) ou son index de collection lorsque vous appelez la méthode **Delete**; une variable objet ne constitue pas un argument valide.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

