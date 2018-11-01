---
title: Workspace.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38f1a7a525a2cf57a98ee3fa015ce29b368aab9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884127"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="11db5-102">Workspace.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="11db5-102">Workspace.Close Method (DAO)</span></span>


<span data-ttu-id="11db5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11db5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11db5-104">Ferme un objet **Workspace** ouvert.</span><span class="sxs-lookup"><span data-stu-id="11db5-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="11db5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11db5-105">Syntax</span></span>

<span data-ttu-id="11db5-106">*expression* . Fermer</span><span class="sxs-lookup"><span data-stu-id="11db5-106">*expression* .Close</span></span>

<span data-ttu-id="11db5-107">*expression* Variable qui représente un objet **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="11db5-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="11db5-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="11db5-108">Remarks</span></span>

<span data-ttu-id="11db5-109">Si l'objet **Workspace** est déjà fermé lorsque vous utilisez la méthode **Close**, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="11db5-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="11db5-110">Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="11db5-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

