---
title: Recordset.Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f7cbd94bfacc91bfe080d33807ca7989c1dca661
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300552"
---
# <a name="recordsetclose-method-dao"></a><span data-ttu-id="86c4c-102">Recordset.Close, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="86c4c-102">Recordset.Close Method (DAO)</span></span>


<span data-ttu-id="86c4c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86c4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86c4c-104">Ferme un objet **Recordset** ouvert.</span><span class="sxs-lookup"><span data-stu-id="86c4c-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86c4c-105">Syntax</span></span>

<span data-ttu-id="86c4c-106">*expression* .Close</span><span class="sxs-lookup"><span data-stu-id="86c4c-106">expression  . Close</span></span>

<span data-ttu-id="86c4c-107">*expression* Variable représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="86c4c-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="86c4c-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="86c4c-108">Remarks</span></span>

<span data-ttu-id="86c4c-109">Si le **jeu d’enregistrements** objet est déjà fermé lorsque vous utilisez **fermer**, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="86c4c-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="86c4c-p101">Si vous essayez de fermer une **connexion** objet alors qu’il a toutes **jeu d’enregistrements** objets, le **jeu d’enregistrements** seront fermés les objets et les mises à jour en attente ou modifications seront annulées . De même, si vous essayez de fermer une **espace de travail** objet alors qu’il a toutes **connexion** objets ceux **connexion** objets seront fermés, qui sera fermer leur **jeu d’enregistrements** objets.</span><span class="sxs-lookup"><span data-stu-id="86c4c-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="86c4c-112">Une alternative à l’utilisation de la méthode **Close** consiste à définir la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="86c4c-112">An alternative to the Close method is to set the value of an object variable to Nothing (Set dbsTemp = Nothing).</span></span>

