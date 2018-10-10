---
title: State, propriété (ADO)
TOCTitle: State Property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2bde03f1d6c7619e8140248b2551002f0453fc9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472347"
---
# <a name="state-property-ado"></a><span data-ttu-id="8c8c1-102">State, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="8c8c1-102">State Property (ADO)</span></span>


<span data-ttu-id="8c8c1-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c8c1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8c8c1-104">Indique, pour tous les objets applicables, si l'état de l'objet est ouvert ou fermé.</span><span class="sxs-lookup"><span data-stu-id="8c8c1-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="8c8c1-105">Indique, pour tous les objets applicables exécutant une méthode asynchrone, si l'état actuel de l'objet est « en cours de connexion », « en cours d'exécution » ou « en cours d'extraction ».</span><span class="sxs-lookup"><span data-stu-id="8c8c1-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c8c1-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8c8c1-106">Return Value</span></span>

<span data-ttu-id="8c8c1-p101">Renvoie une valeur de type **Long** pouvant être une valeur [ObjectStateEnum](objectstateenum.md). La valeur par défaut est **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="8c8c1-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c8c1-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="8c8c1-109">Remarks</span></span>

<span data-ttu-id="8c8c1-110">Vous pouvez utiliser à tout moment la propriété **State** pour déterminer l'état actuel d'un objet donné.</span><span class="sxs-lookup"><span data-stu-id="8c8c1-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="8c8c1-p102">La propriété **State** de l'objet peut présenter plusieurs valeurs associées. Par exemple, si une instruction est en cours d'exécution, cette propriété aura la valeur **adStateOpen** associée à **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="8c8c1-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="8c8c1-113">La propriété **State** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8c8c1-113">The **State** property is read-only.</span></span>

