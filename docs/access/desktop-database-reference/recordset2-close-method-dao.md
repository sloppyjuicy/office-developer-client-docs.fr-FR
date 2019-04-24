---
title: Recordset2. Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 178dec604a185da94493e6d586249bd2a633899c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307384"
---
# <a name="recordset2close-method-dao"></a><span data-ttu-id="f0a9c-102">Recordset2. Close, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="f0a9c-102">Recordset2.Close method (DAO)</span></span>


<span data-ttu-id="f0a9c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0a9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0a9c-104">Ferme un objet **Recordset** ouvert.</span><span class="sxs-lookup"><span data-stu-id="f0a9c-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a9c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0a9c-105">Syntax</span></span>

<span data-ttu-id="f0a9c-106">*expression* . Proches</span><span class="sxs-lookup"><span data-stu-id="f0a9c-106">*expression* .Close</span></span>

<span data-ttu-id="f0a9c-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="f0a9c-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0a9c-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0a9c-108">Remarks</span></span>

<span data-ttu-id="f0a9c-109">Si l'objet **Recordset** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="f0a9c-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="f0a9c-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span><span class="sxs-lookup"><span data-stu-id="f0a9c-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="f0a9c-112">Une autre solution consiste \*\*\*\* à définir la valeur d'une variable d'objet sur **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="f0a9c-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

