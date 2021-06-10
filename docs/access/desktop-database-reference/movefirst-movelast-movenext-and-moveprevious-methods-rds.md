---
title: Méthodes MoveFirst, MoveLast, MoveNext et MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288685"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="e9968-102">Méthodes MoveFirst, MoveLast, MoveNext et MovePrevious (RDS)</span><span class="sxs-lookup"><span data-stu-id="e9968-102">MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)</span></span>

<span data-ttu-id="e9968-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9968-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9968-104">Accède au premier ou dernier enregistrement, à l’enregistrement suivant ou précédent d’un objet [Recordset](recordset-object-ado.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="e9968-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9968-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9968-105">Syntax</span></span>

<span data-ttu-id="e9968-106">*DataControl*. Recordset. {</span><span class="sxs-lookup"><span data-stu-id="e9968-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="e9968-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="e9968-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="e9968-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9968-108">Parameters</span></span>

|<span data-ttu-id="e9968-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e9968-109">Parameter</span></span>|<span data-ttu-id="e9968-110">Description</span><span class="sxs-lookup"><span data-stu-id="e9968-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e9968-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="e9968-111">*DataControl*</span></span> |<span data-ttu-id="e9968-112">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="e9968-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e9968-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="e9968-113">Remarks</span></span>

<span data-ttu-id="e9968-114">Vous pouvez utiliser les **méthodes Move** avec **rdS. Objet DataControl** pour naviguer dans les enregistrements de données dans les contrôles liés aux données sur une page web.</span><span class="sxs-lookup"><span data-stu-id="e9968-114">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> 

<span data-ttu-id="e9968-115">Supposons, par exemple, que vous affichez un objet **Recordset** dans une grille en le liant à un objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="e9968-115">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="e9968-116">Vous pouvez ensuite inclure des boutons Premier, Dernier, Suivant et Précédent sur lesquels les utilisateurs peuvent cliquer pour accéder au premier ou dernier enregistrement, ou encore à l'enregistrement suivant ou précédent de l'objet **Recordset** affiché.</span><span class="sxs-lookup"><span data-stu-id="e9968-116">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="e9968-117">Pour ce faire, appelez les méthodes **MoveFirst**, **MoveLast**, **MoveNext** et **MovePrevious** de l'objet **RDS.DataControl** dans les procédures onClick, respectivement pour les boutons Premier, Dernier, Suivant et Précédent.</span><span class="sxs-lookup"><span data-stu-id="e9968-117">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="e9968-118">L' [exemple du Carnet d'adresses](address-book-navigation-buttons.md) illustre cette procédure.</span><span class="sxs-lookup"><span data-stu-id="e9968-118">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

