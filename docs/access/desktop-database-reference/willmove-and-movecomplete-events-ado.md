---
title: WillMove et MoveComplete, événements (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306053"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="70288-102">WillMove et MoveComplete, événements (ADO)</span><span class="sxs-lookup"><span data-stu-id="70288-102">WillMove and MoveComplete events (ADO)</span></span>

<span data-ttu-id="70288-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70288-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70288-p101">L'événement **WillMove** est appelé avant qu'une opération en attente modifie la position active dans l'objet [Recordset](recordset-object-ado.md). À l'inverse, l'événement **MoveComplete** est appelé après la modification de la position active dans l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="70288-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="70288-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70288-106">Syntax</span></span>

<span data-ttu-id="70288-107">WillMove *adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="70288-107">WillMove *adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="70288-108">MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="70288-108">MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="70288-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70288-109">Parameters</span></span>

|<span data-ttu-id="70288-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="70288-110">Parameter</span></span>|<span data-ttu-id="70288-111">Description</span><span class="sxs-lookup"><span data-stu-id="70288-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="70288-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="70288-112">*adReason*</span></span> |<span data-ttu-id="70288-p102">Valeur [EventReasonEnum](eventreasonenum.md) indiquant la raison de cet événement. Les valeurs possibles sont **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** et **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="70288-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>|
|<span data-ttu-id="70288-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="70288-115">*pError*</span></span> |<span data-ttu-id="70288-p103">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="70288-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="70288-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="70288-118">*adStatus*</span></span> |<span data-ttu-id="70288-119">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="70288-119">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="70288-120">Lorsque **WillMove** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement.</span><span class="sxs-lookup"><span data-stu-id="70288-120">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="70288-121">Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="70288-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="70288-122">Lorsque **MoveComplete** est appelé, ce paramètre a la valeur **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement ou **adStatusErrorsOccurred** si cette dernière a échoué.</span><span class="sxs-lookup"><span data-stu-id="70288-122">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="70288-123">Avant que **WillMove** soit retourné, définissez ce paramètre à **adStatusCancel** pour demander l'annulation de l'opération en attente ou à adStatusUnwantedEvent pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="70288-123">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="70288-124">Avant que **MoveComplete** soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="70288-124">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="70288-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="70288-125">*pRecordset*</span></span> |<span data-ttu-id="70288-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span><span class="sxs-lookup"><span data-stu-id="70288-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="70288-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="70288-128">Remarks</span></span>

<span data-ttu-id="70288-129">Un **événement WillMove** ou **MoveComplete** peut se produire en raison des opérations **recordset suivantes** :</span><span class="sxs-lookup"><span data-stu-id="70288-129">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations:</span></span>

- [<span data-ttu-id="70288-130">Open</span><span class="sxs-lookup"><span data-stu-id="70288-130">Open</span></span>](open-method-ado-recordset.md)
- [<span data-ttu-id="70288-131">Move</span><span class="sxs-lookup"><span data-stu-id="70288-131">Move</span></span>](move-method-ado.md)
- [<span data-ttu-id="70288-132">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="70288-132">MoveFirst</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="70288-133">MoveLast</span><span class="sxs-lookup"><span data-stu-id="70288-133">MoveLast</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="70288-134">MoveNext</span><span class="sxs-lookup"><span data-stu-id="70288-134">MoveNext</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [<span data-ttu-id="70288-135">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="70288-135">MovePrevious</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="70288-136">AddNew</span><span class="sxs-lookup"><span data-stu-id="70288-136">AddNew</span></span>](addnew-method-ado.md)
- [<span data-ttu-id="70288-137">Actualiser</span><span class="sxs-lookup"><span data-stu-id="70288-137">Requery</span></span>](requery-method-ado.md)

<span data-ttu-id="70288-138">Ces événements peuvent se produire en raison des propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="70288-138">These events may occur because of the following properties:</span></span>

- [<span data-ttu-id="70288-139">Filtre</span><span class="sxs-lookup"><span data-stu-id="70288-139">Filter</span></span>](filter-property-ado.md)
- [<span data-ttu-id="70288-140">Index</span><span class="sxs-lookup"><span data-stu-id="70288-140">Index</span></span>](index-property-ado.md)
- [<span data-ttu-id="70288-141">Bookmark</span><span class="sxs-lookup"><span data-stu-id="70288-141">Bookmark</span></span>](bookmark-property-ado.md)
- [<span data-ttu-id="70288-142">AbsolutePage</span><span class="sxs-lookup"><span data-stu-id="70288-142">AbsolutePage</span></span>](absolutepage-property-ado.md)
- [<span data-ttu-id="70288-143">AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="70288-143">AbsolutePosition</span></span>](absoluteposition-property-ado.md)

<span data-ttu-id="70288-144">Ils sont également générés si un objet **Recordset** enfant possède des événements relatifs à **Recordset** et que l'objet **Recordset** parent est déplacé.</span><span class="sxs-lookup"><span data-stu-id="70288-144">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="70288-145">Vous devez affecter au paramètre *adStatus* la valeur **adStatusUnwantedEvent** pour chaque valeur possible du paramètre *adReason* afin d'empêcher définitivement les notifications des événements comprenant un paramètre *adReason*.</span><span class="sxs-lookup"><span data-stu-id="70288-145">You must set the *adStatus* parameter to **adStatusUnwantedEvent** for each possible *adReason* value in order to completely stop event notification for any event that includes an *adReason* parameter.</span></span>

