---
title: Recordset. Cancel, méthode (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300811"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="c2c68-102">Recordset. Cancel, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c2c68-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="c2c68-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2c68-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c68-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2c68-104">Syntax</span></span>

<span data-ttu-id="c2c68-105">*expression* . Annuler</span><span class="sxs-lookup"><span data-stu-id="c2c68-105">*expression* .Cancel</span></span>

<span data-ttu-id="c2c68-106">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c2c68-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2c68-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2c68-107">Remarks</span></span>

<span data-ttu-id="c2c68-108">Utilisez la méthode **Cancel** pour mettre fin à l'exécution d'un appel asynchrone de méthode **Execute** ou **OpenConnection** (autrement dit, la méthode a été appelée avec l'option dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="c2c68-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="c2c68-109">**Cancel** renvoie une erreur d'exécution si dbRunAsync n'a pas été utilisé dans la méthode que vous essayez de terminer.</span><span class="sxs-lookup"><span data-stu-id="c2c68-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

