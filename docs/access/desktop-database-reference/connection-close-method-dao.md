---
title: Méthode Connection.Close, mais (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf99abf97a2eb1b88e7056a36c160eb774959719
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717215"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="2478c-102">Méthode Connection.Close, mais (DAO)</span><span class="sxs-lookup"><span data-stu-id="2478c-102">Connection.Close method (DAO)</span></span>


<span data-ttu-id="2478c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2478c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2478c-104">Ferme un objet **Connection** ouvert.</span><span class="sxs-lookup"><span data-stu-id="2478c-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2478c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2478c-105">Syntax</span></span>

<span data-ttu-id="2478c-106">*expression* . Fermer</span><span class="sxs-lookup"><span data-stu-id="2478c-106">*expression* .Close</span></span>

<span data-ttu-id="2478c-107">*expression* Variable qui représente un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="2478c-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2478c-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="2478c-108">Remarks</span></span>

<span data-ttu-id="2478c-109">Si l'objet **Recordset** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="2478c-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="2478c-p101">Si vous tentez de fermer un objet **Connection** alors que celui-ci possède des objets **Recordset** ouverts, les objets **Recordset** ouverts seront fermés et toute mise à jour ou modification en attente sera annulée. De la même façon, si vous essayez de fermer un objet **Workspace** qui possède des objets **Connection** ouverts, ces objets **Connection** seront fermés de même que les objets **Recordset** qu'ils comportent.</span><span class="sxs-lookup"><span data-stu-id="2478c-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="2478c-112">Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="2478c-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

