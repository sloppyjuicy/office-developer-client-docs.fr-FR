---
title: QueryDef. Cancel, méthode (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301119"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="c02fa-102">QueryDef. Cancel, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c02fa-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="c02fa-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c02fa-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c02fa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c02fa-104">Syntax</span></span>

<span data-ttu-id="c02fa-105">*expression* . Annuler</span><span class="sxs-lookup"><span data-stu-id="c02fa-105">*expression* .Cancel</span></span>

<span data-ttu-id="c02fa-106">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="c02fa-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c02fa-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="c02fa-107">Remarks</span></span>

<span data-ttu-id="c02fa-108">Utilisez la méthode **Cancel** pour mettre fin à l'exécution d'un appel asynchrone de méthode **Execute** ou **OpenConnection** (autrement dit, la méthode a été appelée avec l'option dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="c02fa-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="c02fa-109">**Cancel** renvoie une erreur d'exécution si dbRunAsync n'a pas été utilisé dans la méthode que vous essayez de terminer.</span><span class="sxs-lookup"><span data-stu-id="c02fa-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

