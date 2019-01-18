---
title: DELETE, méthode (Collection de paramètres ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704573"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="4803b-102">DELETE, méthode (Collection de paramètres ADO)</span><span class="sxs-lookup"><span data-stu-id="4803b-102">Delete method (ADO Parameters Collection)</span></span>

<span data-ttu-id="4803b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4803b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4803b-104">Supprime un objet de la collection [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4803b-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4803b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4803b-105">Syntax</span></span>

<span data-ttu-id="4803b-106">*Paramètres*. Supprimer *l’Index*</span><span class="sxs-lookup"><span data-stu-id="4803b-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="4803b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4803b-107">Parameters</span></span>

|<span data-ttu-id="4803b-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="4803b-108">Parameter</span></span>|<span data-ttu-id="4803b-109">Description</span><span class="sxs-lookup"><span data-stu-id="4803b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4803b-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="4803b-110">*Index*</span></span> |<span data-ttu-id="4803b-111">Valeur de type **String** contenant le nom de l'objet que vous voulez supprimer ou la position ordinale (index) de l'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="4803b-111">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4803b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4803b-112">Remarks</span></span>

<span data-ttu-id="4803b-p101">L'utilisation de la méthode **Delete** sur une collection permet de supprimer l'un des objets figurant dans cette collection. Cette méthode est uniquement disponible pour la collection **Parameters** d'un objet [Command](command-object-ado.md). Vous devez utiliser la propriété [Name](parameter-object-ado.md) de l'objet [Parameter](name-property-ado.md) ou son index de collection lorsque vous appelez la méthode **Delete**; une variable objet ne constitue pas un argument valide.</span><span class="sxs-lookup"><span data-stu-id="4803b-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

