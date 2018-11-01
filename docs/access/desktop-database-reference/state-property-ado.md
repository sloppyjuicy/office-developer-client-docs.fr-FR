---
title: State, propriété (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d8ea3738465ed9bfc10cbabdf355036f7c160f66
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886612"
---
# <a name="state-property-ado"></a><span data-ttu-id="fbc9a-102">State, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="fbc9a-102">State property (ADO)</span></span>


<span data-ttu-id="fbc9a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbc9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fbc9a-104">Indique, pour tous les objets applicables, si l'état de l'objet est ouvert ou fermé.</span><span class="sxs-lookup"><span data-stu-id="fbc9a-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="fbc9a-105">Indique, pour tous les objets applicables exécutant une méthode asynchrone, si l'état actuel de l'objet est « en cours de connexion », « en cours d'exécution » ou « en cours d'extraction ».</span><span class="sxs-lookup"><span data-stu-id="fbc9a-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbc9a-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fbc9a-106">Return value</span></span>

<span data-ttu-id="fbc9a-p101">Renvoie une valeur de type **Long** pouvant être une valeur [ObjectStateEnum](objectstateenum.md). La valeur par défaut est **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="fbc9a-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc9a-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="fbc9a-109">Remarks</span></span>

<span data-ttu-id="fbc9a-110">Vous pouvez utiliser à tout moment la propriété **State** pour déterminer l'état actuel d'un objet donné.</span><span class="sxs-lookup"><span data-stu-id="fbc9a-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="fbc9a-p102">La propriété **State** de l'objet peut présenter plusieurs valeurs associées. Par exemple, si une instruction est en cours d'exécution, cette propriété aura la valeur **adStateOpen** associée à **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="fbc9a-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="fbc9a-113">La propriété **State** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fbc9a-113">The **State** property is read-only.</span></span>

