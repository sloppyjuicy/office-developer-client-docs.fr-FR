---
title: Propriété QueryDef.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 98e85d37-de50-afe1-dcca-01623546e0ad
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197953(v=office.15)
ms:contentKeyID: 48546505
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053584
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 60c0663eaa6857801555c6ce05f4256cfe4c290f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303415"
---
# <a name="querydefstillexecuting-property-dao"></a><span data-ttu-id="f1e68-102">Propriété QueryDef.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="f1e68-102">QueryDef.StillExecuting property (DAO)</span></span>


<span data-ttu-id="f1e68-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1e68-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e68-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1e68-104">Syntax</span></span>

<span data-ttu-id="f1e68-105">*.* StillExecuting</span><span class="sxs-lookup"><span data-stu-id="f1e68-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="f1e68-106">*expression* Variable représentant un objet **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="f1e68-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1e68-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1e68-107">Remarks</span></span>

<span data-ttu-id="f1e68-p101">Utilisez la propriété **StillExecuting** pour déterminer si la dernière méthode **[Execute](querydef-execute-method-dao.md)** ou **[OpenConnection](dbengine-openconnection-method-dao.md)** asynchrone appelée (c.-à-d. une méthode exécutée avec l'option **dbRunAsync**) est terminée. Il est impossible d'accéder à tout objet renvoyé tant que la propriété **StillExecuting** a la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="f1e68-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **[Execute](querydef-execute-method-dao.md)** or **[OpenConnection](dbengine-openconnection-method-dao.md)** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="f1e68-p102">Dès que la propriété **StillExecuting** renvoie **False**, à la suite de l'appel de **OpenConnection** qui retourne l'objet **[Connection](connection-object-dao.md)** associé, il est possible de référencer l'objet. Tant que la propriété **StillExecuting** conserve la valeur **True**, vous ne pouvez pas faire référence à l'objet mais simplement lire la propriété **StillExecuting**.</span><span class="sxs-lookup"><span data-stu-id="f1e68-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **[Connection](connection-object-dao.md)** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="f1e68-112">Utilisez la méthode **[Cancel](connection-cancel-method-dao.md)** pour mettre fin à l'exécution d'une tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="f1e68-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

