---
title: WillMove et MoveComplete, événements (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5388601f1ac88e281a6abc5cfe1e644bdeebef28
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923566"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="bc8ef-102">WillMove et MoveComplete, événements (ADO)</span><span class="sxs-lookup"><span data-stu-id="bc8ef-102">WillMove and MoveComplete events (ADO)</span></span>


<span data-ttu-id="bc8ef-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc8ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc8ef-p101">L'événement **WillMove** est appelé avant qu'une opération en attente modifie la position active dans l'objet [Recordset](recordset-object-ado.md). À l'inverse, l'événement **MoveComplete** est appelé après la modification de la position active dans l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8ef-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc8ef-106">Syntax</span></span>

<span data-ttu-id="bc8ef-107">WillMove*adReason*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="bc8ef-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="bc8ef-108">MoveComplete*adReason*, *pError*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="bc8ef-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="bc8ef-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc8ef-109">Parameters</span></span>

  - <span data-ttu-id="bc8ef-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="bc8ef-110">*adReason*</span></span>

  - <span data-ttu-id="bc8ef-p102">Valeur [EventReasonEnum](eventreasonenum.md) indiquant la raison de cet événement. Les valeurs possibles sont **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** et **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>

  - <span data-ttu-id="bc8ef-113">*pError*</span><span class="sxs-lookup"><span data-stu-id="bc8ef-113">*pError*</span></span>

  - <span data-ttu-id="bc8ef-p103">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="bc8ef-116">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="bc8ef-116">*adStatus*</span></span>

  - [<span data-ttu-id="bc8ef-117">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="bc8ef-117">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="bc8ef-p104">Lorsque **WillMove** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-p104">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="bc8ef-120">Lorsque **MoveComplete** est appelé, ce paramètre a la valeur **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement ou **adStatusErrorsOccurred** si cette dernière a échoué.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-120">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="bc8ef-121">Avant que **WillMove** soit retourné, définissez ce paramètre à **adStatusCancel** pour demander l'annulation de l'opération en attente ou à adStatusUnwantedEvent pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-121">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="bc8ef-122">Avant que **MoveComplete** soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-122">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="bc8ef-123">*Connection*</span><span class="sxs-lookup"><span data-stu-id="bc8ef-123">*pRecordset*</span></span>

  - <span data-ttu-id="bc8ef-124">Objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bc8ef-124">A [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="bc8ef-125">Le **jeu d’enregistrements** pour laquelle cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-125">The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc8ef-126">Notes</span><span class="sxs-lookup"><span data-stu-id="bc8ef-126">Remarks</span></span>

<span data-ttu-id="bc8ef-p106">Un événement **WillMove** ou **MoveComplete** peut se produire suite aux opérations suivantes sur l'objet **Recordset**: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md) et [Requery](requery-method-ado.md). Ces événements peuvent être déclenchés par l'utilisation des propriétés suivantes : [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) et [AbsolutePosition](absoluteposition-property-ado.md). Ils sont également générés si un objet **Recordset** enfant possède des événements relatifs à **Recordset** et que l'objet **Recordset** parent est déplacé.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-p106">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md), and [Requery](requery-method-ado.md). These events may occur because of the following properties: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), and [AbsolutePosition](absoluteposition-property-ado.md). These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="bc8ef-130">Vous devez affecter au paramètre **adStatus** la valeur **adStatusUnwantedEvent** pour chaque valeur possible du paramètre adReason afin d'empêcher définitivement les notifications des événements comprenant un paramètre adReason.</span><span class="sxs-lookup"><span data-stu-id="bc8ef-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible adReason value in order to completely stop event notification for any event that includes an adReason parameter.</span></span>

