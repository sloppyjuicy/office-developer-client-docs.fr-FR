---
title: Recordset2.Cancel, méthode (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307412"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="da0ac-102">Recordset2.Cancel, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="da0ac-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="da0ac-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da0ac-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="da0ac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da0ac-104">Syntax</span></span>

<span data-ttu-id="da0ac-105">*.* Annuler</span><span class="sxs-lookup"><span data-stu-id="da0ac-105">*expression* .Cancel</span></span>

<span data-ttu-id="da0ac-106">*expression* Expression qui renvoie un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="da0ac-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="da0ac-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="da0ac-107">Remarks</span></span>

<span data-ttu-id="da0ac-108">Utilisez la **méthode Cancel** pour terminer l’exécution d’un appel asynchrone de méthode **Execute** ou **OpenConnection** (autrement dit, la méthode a été invoquée avec l’option dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="da0ac-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="da0ac-109">**L’annulation** retourne une erreur d’utilisation si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez de terminer.</span><span class="sxs-lookup"><span data-stu-id="da0ac-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

