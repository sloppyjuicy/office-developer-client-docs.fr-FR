---
title: Propriété Recordset2.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55a5adf32c64735cb773e3f1da5de79703a2a3cc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930146"
---
# <a name="recordset2stillexecuting-property-dao"></a><span data-ttu-id="de2de-102">Propriété Recordset2.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="de2de-102">Recordset2.StillExecuting property (DAO)</span></span>


<span data-ttu-id="de2de-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de2de-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="de2de-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de2de-104">Syntax</span></span>

<span data-ttu-id="de2de-105">*expression* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="de2de-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="de2de-106">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="de2de-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de2de-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="de2de-107">Remarks</span></span>

<span data-ttu-id="de2de-p101">Utilisez la propriété **StillExecuting** pour déterminer si la dernière méthode **Execute** ou **OpenConnection** asynchrone appelée (c.-à-d. une méthode exécutée avec l'option **dbRunAsync**) est terminée. Il est impossible d'accéder à tout objet renvoyé tant que la propriété **StillExecuting** a la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="de2de-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="de2de-p102">Dès que la propriété **StillExecuting** renvoie **False**, à la suite de l'appel de **OpenConnection** qui retourne l'objet **Connection** associé, il est possible de référencer l'objet. Tant que la propriété **StillExecuting** conserve la valeur **True**, vous ne pouvez pas faire référence à l'objet mais simplement lire la propriété **StillExecuting**.</span><span class="sxs-lookup"><span data-stu-id="de2de-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="de2de-112">Utilisez la méthode **[Cancel](connection-cancel-method-dao.md)** pour mettre fin à l'exécution d'une tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="de2de-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

