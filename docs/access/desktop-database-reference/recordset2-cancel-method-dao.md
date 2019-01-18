---
title: Méthode Recordset2.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708423"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="f83e5-102">Méthode Recordset2.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="f83e5-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="f83e5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f83e5-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f83e5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f83e5-104">Syntax</span></span>

<span data-ttu-id="f83e5-105">*expression* . Annuler</span><span class="sxs-lookup"><span data-stu-id="f83e5-105">*expression* .Cancel</span></span>

<span data-ttu-id="f83e5-106">*expression* Expression qui renvoie un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="f83e5-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f83e5-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="f83e5-107">Remarks</span></span>

<span data-ttu-id="f83e5-108">Utilisez la méthode **Cancel** pour mettre fin à l’exécution d’un appel de méthode **Execute** ou **OpenConnection** asynchrone (autrement dit, la méthode a été appelée avec l’option dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="f83e5-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="f83e5-109">**Annuler** renvoie une erreur d’exécution si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez d’interrompre.</span><span class="sxs-lookup"><span data-stu-id="f83e5-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

