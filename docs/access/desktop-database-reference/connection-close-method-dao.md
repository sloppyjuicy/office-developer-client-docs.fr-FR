---
title: Connection.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4cc4230c7d647d58c0f30bd8351118e6c44198a8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879696"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="69cf9-102">Connection.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="69cf9-102">Connection.Close Method (DAO)</span></span>


<span data-ttu-id="69cf9-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69cf9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69cf9-104">Ferme un objet **Connection** ouvert.</span><span class="sxs-lookup"><span data-stu-id="69cf9-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="69cf9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69cf9-105">Syntax</span></span>

<span data-ttu-id="69cf9-106">*expression* . Fermer</span><span class="sxs-lookup"><span data-stu-id="69cf9-106">*expression* .Close</span></span>

<span data-ttu-id="69cf9-107">*expression* Variable qui représente un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="69cf9-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="69cf9-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="69cf9-108">Remarks</span></span>

<span data-ttu-id="69cf9-109">Si l'objet **Recordset** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="69cf9-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="69cf9-p101">Si vous tentez de fermer un objet **Connection** alors que celui-ci possède des objets **Recordset** ouverts, les objets **Recordset** ouverts seront fermés et toute mise à jour ou modification en attente sera annulée. De la même façon, si vous essayez de fermer un objet **Workspace** qui possède des objets **Connection** ouverts, ces objets **Connection** seront fermés de même que les objets **Recordset** qu'ils comportent.</span><span class="sxs-lookup"><span data-stu-id="69cf9-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="69cf9-112">Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="69cf9-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

