---
title: Recordset2.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f20c10ac6bb6fc313ffecb56b0d2852c3b488c26
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471140"
---
# <a name="recordset2close-method-dao"></a><span data-ttu-id="4a88e-102">Recordset2.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="4a88e-102">Recordset2.Close Method (DAO)</span></span>


<span data-ttu-id="4a88e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a88e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4a88e-104">Ferme un objet **Recordset** ouvert.</span><span class="sxs-lookup"><span data-stu-id="4a88e-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a88e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a88e-105">Syntax</span></span>

<span data-ttu-id="4a88e-106">*expression* . Fermer</span><span class="sxs-lookup"><span data-stu-id="4a88e-106">*expression* .Close</span></span>

<span data-ttu-id="4a88e-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="4a88e-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a88e-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a88e-108">Remarks</span></span>

<span data-ttu-id="4a88e-109">Si l'objet **Recordset** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="4a88e-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="4a88e-p101">Si vous tentez de fermer un objet **Connection** alors que celui-ci possède des objets **Recordset** ouverts, les objets **Recordset** ouverts seront fermés et toute mise à jour ou modification en attente sera annulée. De la même façon, si vous essayez de fermer un objet **Workspace** qui possède des objets **Connection** ouverts, ces objets **Connection** seront fermés de même que les objets **Recordset** qu'ils comportent.</span><span class="sxs-lookup"><span data-stu-id="4a88e-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="4a88e-112">Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="4a88e-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

