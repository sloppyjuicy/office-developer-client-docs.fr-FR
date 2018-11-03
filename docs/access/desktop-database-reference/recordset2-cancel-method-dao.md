---
title: Méthode Recordset2.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 159f476b592a8c944df2dc4570d84377c89b5043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929229"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="3fb75-102">Méthode Recordset2.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="3fb75-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="3fb75-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fb75-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb75-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fb75-104">Syntax</span></span>

<span data-ttu-id="3fb75-105">*expression* . Annuler</span><span class="sxs-lookup"><span data-stu-id="3fb75-105">*expression* .Cancel</span></span>

<span data-ttu-id="3fb75-106">*expression* Expression qui renvoie un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3fb75-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fb75-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="3fb75-107">Remarks</span></span>

<span data-ttu-id="3fb75-108">Utilisez la méthode **Cancel** pour mettre fin à l’exécution d’un appel de méthode **Execute** ou **OpenConnection** asynchrone (autrement dit, la méthode a été appelée avec l’option dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="3fb75-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="3fb75-109">**Annuler** renvoie une erreur d’exécution si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez d’interrompre.</span><span class="sxs-lookup"><span data-stu-id="3fb75-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

