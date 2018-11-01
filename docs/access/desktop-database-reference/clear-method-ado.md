---
title: Clear, méthode - ActiveX Data Objects (ADO)
TOCTitle: Clear Method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 864c31a75514b4e8c56383672b196a4e62c4ec8f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876784"
---
# <a name="clear-method-ado"></a><span data-ttu-id="ee837-102">Clear, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ee837-102">Clear Method (ADO)</span></span>


<span data-ttu-id="ee837-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee837-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee837-104">Supprime tous les objets **Error** de la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="ee837-104">Removes all the **Error** objects from the **Errors** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee837-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee837-105">Syntax</span></span>

<span data-ttu-id="ee837-106">*Erreurs*. Effacer</span><span class="sxs-lookup"><span data-stu-id="ee837-106">*Errors*.Clear</span></span>

## <a name="remarks"></a><span data-ttu-id="ee837-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ee837-107">Remarks</span></span>

<span data-ttu-id="ee837-p101">Utilisez la méthode **Clear** de la collection [Errors](errors-collection-ado.md) pour supprimer tous les objets [Error](error-object-ado.md) existants de la collection. En cas d'erreur, ADO supprime automatiquement le contenu de la collection **Errors** et la remplit d'objets **Error** liés à la nouvelle erreur.</span><span class="sxs-lookup"><span data-stu-id="ee837-p101">Use the **Clear** method on the [Errors](errors-collection-ado.md) collection to remove all existing [Error](error-object-ado.md) objects from the collection. When an error occurs, ADO automatically clears the **Errors** collection and fills it with **Error** objects based on the new error.</span></span>

<span data-ttu-id="ee837-p102">Certaines propriétés et méthodes retournent des avertissements qui apparaissent en tant qu'objets **Error** dans la collection **Errors** sans pour autant arrêter l'exécution d'un programme. Avant d'appeler les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md) ou la méthode [Open](open-method-ado-connection.md) sur un objet [Connection](connection-object-ado.md) ou encore avant de définir la propriété [Filter](filter-property-ado.md) sur un objet **Recordset**, appelez la méthode **Clear** sur la collection **Errors**. Ainsi, vous pourrez lire la propriété [Count](count-property-ado.md) de la collection **Errors** afin de vérifier les avertissements retournés.</span><span class="sxs-lookup"><span data-stu-id="ee837-p102">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a [Connection](connection-object-ado.md) object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

