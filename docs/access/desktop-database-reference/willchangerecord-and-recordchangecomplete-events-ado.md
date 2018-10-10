---
title: WillChangeRecord et RecordChangeComplete, événements (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete Events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5dca190dca19654314df3944b4b1696874f9afaa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470019"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a><span data-ttu-id="87b4a-102">WillChangeRecord et RecordChangeComplete, événements (ADO)</span><span class="sxs-lookup"><span data-stu-id="87b4a-102">WillChangeRecord and RecordChangeComplete Events (ADO)</span></span>


<span data-ttu-id="87b4a-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="87b4a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="87b4a-p101">L'événement **WillChangeRecord** est appelé avant qu'un ou plusieurs enregistrements (lignes) de l'objet [Recordset](recordset-object-ado.md) soient modifiés. À l'inverse, l'événement **RecordChangeComplete** est appelé après la modification d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="87b4a-p101">The **WillChangeRecord** event is called before one or more records (rows) in the [Recordset](recordset-object-ado.md) change. The **RecordChangeComplete** event is called after one or more records change.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b4a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87b4a-106">Syntax</span></span>

<span data-ttu-id="87b4a-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="87b4a-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="87b4a-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="87b4a-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="87b4a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87b4a-109">Parameters</span></span>

  - <span data-ttu-id="87b4a-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="87b4a-110">*adReason*</span></span>

  - <span data-ttu-id="87b4a-p102">Valeur [EventReasonEnum](eventreasonenum.md) indiquant la raison de cet événement. Les valeurs possibles sont **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** et **adRsnFirstChange**.</span><span class="sxs-lookup"><span data-stu-id="87b4a-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, or **adRsnFirstChange**.</span></span>

  - <span data-ttu-id="87b4a-113">*cRecords*</span><span class="sxs-lookup"><span data-stu-id="87b4a-113">*cRecords*</span></span>

  - <span data-ttu-id="87b4a-114">Valeur de type **Long** indiquant le nombre d'enregistrements en cours de modification (c'est-à-dire affectés par l'opération).</span><span class="sxs-lookup"><span data-stu-id="87b4a-114">A **Long** value that indicates the number of records changing (affected).</span></span>

  - <span data-ttu-id="87b4a-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="87b4a-115">*pError*</span></span>

  - <span data-ttu-id="87b4a-p103">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="87b4a-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="87b4a-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="87b4a-118">*adStatus*</span></span>

  - [<span data-ttu-id="87b4a-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="87b4a-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="87b4a-p104">Lorsque **WillChangerecord** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="87b4a-p104">When **WillChangeRecord** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="87b4a-122">Lorsque **RecordChangeComplete** est appelé, ce paramètre a la valeur **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement ou **adStatusErrorsOccurred** si cette dernière a échoué.</span><span class="sxs-lookup"><span data-stu-id="87b4a-122">When **RecordChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="87b4a-123">Avant que **WillChangeRecord** soit retourné, définissez ce paramètre à **adStatusCancel** pour demander l'annulation de l'opération à l'origine de l'événement ou à adStatusUnwantedEvent pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="87b4a-123">Before **WillChangeRecord** returns, set this parameter to **adStatusCancel** to request cancellation of the operation that caused this event or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="87b4a-124">Avant que **RecordChangeComplete** soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="87b4a-124">Before **RecordChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="87b4a-125">*Connection*</span><span class="sxs-lookup"><span data-stu-id="87b4a-125">*pRecordset*</span></span>

  - <span data-ttu-id="87b4a-126">Objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="87b4a-126">A **Recordset** object.</span></span> <span data-ttu-id="87b4a-127">Le **jeu d’enregistrements** pour laquelle cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="87b4a-127">The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="87b4a-128">Notes</span><span class="sxs-lookup"><span data-stu-id="87b4a-128">Remarks</span></span>

<span data-ttu-id="87b4a-129">Il se peut qu'un événement **WillChangeRecord** ou **RecordChangeComplete** se produise pour le premier champ modifié dans une ligne lorsque les opérations suivantes sont effectuées sur l'objet **Recordset**: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) et [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="87b4a-129">A **WillChangeRecord** or **RecordChangeComplete** event may occur for the first changed field in a row due to the following **Recordset** operations: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [CancelBatch](cancelbatch-method-ado.md).</span></span> <span data-ttu-id="87b4a-130">La valeur de l' **objet Recordset** [CursorType](cursortype-property-ado.md) détermine les opérations qui déclenchent les événements.</span><span class="sxs-lookup"><span data-stu-id="87b4a-130">The value of the **Recordset** [CursorType](cursortype-property-ado.md) determines which operations cause the events to occur.</span></span>

<span data-ttu-id="87b4a-131">Pendant l’événement **WillChangeRecord** , la propriété [Filter](filter-property-ado.md) de **jeu d’enregistrements** est définie à **adFilterAffectedRecords**.</span><span class="sxs-lookup"><span data-stu-id="87b4a-131">During the **WillChangeRecord** event, the **Recordset** [Filter](filter-property-ado.md) property is set to **adFilterAffectedRecords**.</span></span> <span data-ttu-id="87b4a-132">Sa valeur n'est pas modifiable lorsque l'événement est en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="87b4a-132">You cannot change this property while processing the event.</span></span>

<span data-ttu-id="87b4a-133">Vous devez affecter la valeur adStatusUnwantedEvent au paramètre adStatus pour chaque valeur possible du paramètre adReason afin d'empêcher définitivement les notifications des événements comprenant un paramètre adReason.</span><span class="sxs-lookup"><span data-stu-id="87b4a-133">You must set the adStatus parameter to adStatusUnwantedEvent for each possible adReason value in order to completely stop event noticiation for any event that includes an adReason parameter.</span></span>

