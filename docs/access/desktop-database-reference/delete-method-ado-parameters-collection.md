---
title: Delete, méthode (collection paraMeters ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294091"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="81a35-102">Delete, méthode (collection paraMeters ADO)</span><span class="sxs-lookup"><span data-stu-id="81a35-102">Delete method (ADO Parameters Collection)</span></span>

<span data-ttu-id="81a35-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81a35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81a35-104">Supprime un objet de la collection [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="81a35-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81a35-105">Syntax</span></span>

<span data-ttu-id="81a35-106">*Paramètres*. Supprimer l' *index*</span><span class="sxs-lookup"><span data-stu-id="81a35-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="81a35-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81a35-107">Parameters</span></span>

|<span data-ttu-id="81a35-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="81a35-108">Parameter</span></span>|<span data-ttu-id="81a35-109">Description</span><span class="sxs-lookup"><span data-stu-id="81a35-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="81a35-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="81a35-110">*Index*</span></span> |<span data-ttu-id="81a35-111">Valeur de type **String** contenant le nom de l'objet que vous voulez supprimer ou la position ordinale (index) de l'objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="81a35-111">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="81a35-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="81a35-112">Remarks</span></span>

<span data-ttu-id="81a35-p101">L’utilisation de la méthode **Delete** sur une collection permet de supprimer l’un des objets figurant dans cette collection. Cette méthode est uniquement disponible pour la collection **Parameters** d’un objet [Command](command-object-ado.md). Vous devez utiliser la propriété [Name](name-property-ado.md) de l’objet [Parameter](parameter-object-ado.md) ou son index de collection lorsque vous appelez la méthode **Delete** ; une variable objet ne constitue pas un argument valide.</span><span class="sxs-lookup"><span data-stu-id="81a35-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

