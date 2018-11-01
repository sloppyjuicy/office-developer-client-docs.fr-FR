---
title: Recordset.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cde31424f409f3b3d152189e3964bc3447cfd53c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871485"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="89e94-102">Recordset.Cancel Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="89e94-102">Recordset.Cancel Method (DAO)</span></span>


<span data-ttu-id="89e94-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89e94-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="89e94-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89e94-104">Syntax</span></span>

<span data-ttu-id="89e94-105">*expression* . Annuler</span><span class="sxs-lookup"><span data-stu-id="89e94-105">*expression* .Cancel</span></span>

<span data-ttu-id="89e94-106">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="89e94-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="89e94-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="89e94-107">Remarks</span></span>

<span data-ttu-id="89e94-108">Utilisez la méthode **Cancel** pour mettre fin à l’exécution d’un appel de méthode **Execute** ou **OpenConnection** asynchrone (autrement dit, la méthode a été appelée avec l’option dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="89e94-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="89e94-109">**Annuler** renvoie une erreur d’exécution si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez d’interrompre.</span><span class="sxs-lookup"><span data-stu-id="89e94-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

