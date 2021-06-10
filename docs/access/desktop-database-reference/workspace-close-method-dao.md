---
title: Workspace.Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305956"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="669ae-102">Workspace.Close, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="669ae-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="669ae-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="669ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="669ae-104">Ferme un objet **Workspace** ouvert.</span><span class="sxs-lookup"><span data-stu-id="669ae-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="669ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="669ae-105">Syntax</span></span>

<span data-ttu-id="669ae-106">*expression* .Close</span><span class="sxs-lookup"><span data-stu-id="669ae-106">*expression* .Close</span></span>

<span data-ttu-id="669ae-107">*expression* Variable qui représente un objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="669ae-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="669ae-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="669ae-108">Remarks</span></span>

<span data-ttu-id="669ae-109">Si l'objet **Workspace** est déjà fermé lorsque vous utilisez la méthode **Close**, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="669ae-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="669ae-110">Une alternative à l’utilisation de la méthode **Close** consiste à définir la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="669ae-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

