---
title: WillChangeRecordset et RecordsetChangeComplete, événements (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete Events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a7bf9a69fd5a648efc86f698e82ca0ba9413a30
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886311"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a><span data-ttu-id="5bc61-102">WillChangeRecordset et RecordsetChangeComplete, événements (ADO)</span><span class="sxs-lookup"><span data-stu-id="5bc61-102">WillChangeRecordset and RecordsetChangeComplete Events (ADO)</span></span>


<span data-ttu-id="5bc61-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bc61-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="5bc61-p101">L'événement **WillChangeRecordset** est appelé avant qu'une opération en attente modifie l'objet [Recordset](recordset-object-ado.md). À l'inverse, l'événement **RecordsetChangeComplete** est appelé après cette modification de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5bc61-p101">The **WillChangeRecordset** event is called before a pending operation changes the [Recordset](recordset-object-ado.md). The **RecordsetChangeComplete** event is called after the **Recordset** has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc61-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bc61-106">Syntax</span></span>

<span data-ttu-id="5bc61-107">WillChangeRecordset*adReason*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="5bc61-107">WillChangeRecordset*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="5bc61-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="5bc61-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="5bc61-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bc61-109">Parameters</span></span>

  - <span data-ttu-id="5bc61-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="5bc61-110">*adReason*</span></span>

  - <span data-ttu-id="5bc61-p102">Valeur [EventReasonEnum](eventreasonenum.md) indiquant la raison de cet événement. Les valeurs possibles sont **adRsnRequery**, **adRsnResynch**, **adRsnClose** et **adRsnOpen**.</span><span class="sxs-lookup"><span data-stu-id="5bc61-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span></span>

  - <span data-ttu-id="5bc61-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="5bc61-113">*adStatus*</span></span>

  - [<span data-ttu-id="5bc61-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="5bc61-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="5bc61-p103">Lorsque **WillChangeRecordset** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="5bc61-p103">When **WillChangeRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="5bc61-117">Lorsque **RecordsetChangeComplete** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement, à **adStatusErrorsOccurred** si cette dernière a échoué ou encore à **adStatusCancel** si l'opération associée à l'événement **WillChangeRecordset** précédemment accepté a été annulée</span><span class="sxs-lookup"><span data-stu-id="5bc61-117">When **RecordsetChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, **adStatusErrorsOccurred** if the operation failed, or **adStatusCancel** if the operation associated with the previously accepted **WillChangeRecordset** event has been canceled.</span></span>
    
    <span data-ttu-id="5bc61-118">Avant que **WillChangeRecordset** soit retourné, définissez ce paramètre à **adStatusCancel** pour demander l'annulation de l'opération en attente ou à adStatusUnwantedEvent pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5bc61-118">Before **WillChangeRecordset** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</span></span>
    
    <span data-ttu-id="5bc61-119">Avant que **WillChangeRecordset** ou que **RecordsetChangeComplete** soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5bc61-119">Before **WillChangeRecordset** or **RecordsetChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="5bc61-120">*pError*</span><span class="sxs-lookup"><span data-stu-id="5bc61-120">*pError*</span></span>

  - <span data-ttu-id="5bc61-p104">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="5bc61-p104">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="5bc61-123">*Connection*</span><span class="sxs-lookup"><span data-stu-id="5bc61-123">*pRecordset*</span></span>

  - <span data-ttu-id="5bc61-124">Objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5bc61-124">A **Recordset** object.</span></span> <span data-ttu-id="5bc61-125">Le **jeu d’enregistrements** pour laquelle cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="5bc61-125">The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc61-126">Notes</span><span class="sxs-lookup"><span data-stu-id="5bc61-126">Remarks</span></span>

<span data-ttu-id="5bc61-127">Les méthodes de **l’objet Recordset** [Requery](requery-method-ado.md) ou [Open](open-method-ado-recordset.md) peut entraîner un **WillChangeRecordset** ou **RecordsetChangeComplete** .</span><span class="sxs-lookup"><span data-stu-id="5bc61-127">A **WillChangeRecordset** or **RecordsetChangeComplete** event may occur due to the **Recordset** [Requery](requery-method-ado.md) or [Open](open-method-ado-recordset.md) methods.</span></span>

<span data-ttu-id="5bc61-p106">Si le fournisseur ne prend pas en charge les signets, une notification d'événement **RecordsetChange** est générée chaque fois que des nouvelles lignes sont extraites du fournisseur. La fréquence de cet événement dépend de la propriété **RecordsetCacheSize**.</span><span class="sxs-lookup"><span data-stu-id="5bc61-p106">If the provider does not support bookmarks, a **RecordsetChange** event notification occurs each time new rows are retrieved from the provider. The frequency of this event depends on the **RecordsetCacheSize** property.</span></span>

<span data-ttu-id="5bc61-130">Vous devez affecter au paramètre **adStatus** la valeur **adStatusUnwantedEvent** pour chaque valeur possible du paramètre **adReason** afin d'empêcher définitivement les notifications des événements comprenant un paramètre **adReason**.</span><span class="sxs-lookup"><span data-stu-id="5bc61-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible **adReason** value in order to completely stop event notification for any event that includes an **adReason** parameter.</span></span>

