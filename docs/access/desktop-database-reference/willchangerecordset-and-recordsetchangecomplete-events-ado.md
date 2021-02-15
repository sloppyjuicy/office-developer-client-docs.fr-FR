---
title: WillChangeRecordset et RecordsetChangeComplete, événements (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfb304f41ada88e1b0546aaa4a54240b931017cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302820"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a><span data-ttu-id="c2614-102">WillChangeRecordset et RecordsetChangeComplete, événements (ADO)</span><span class="sxs-lookup"><span data-stu-id="c2614-102">WillChangeRecordset and RecordsetChangeComplete events (ADO)</span></span>

<span data-ttu-id="c2614-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2614-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2614-104">L'événement **WillChangeRecordset** est appelé avant qu'une opération en attente modifie l'objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c2614-104">The **WillChangeRecordset** event is called before a pending operation changes the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="c2614-105">À l’inverse, l’événement **RecordsetChangeComplete** est appelé après cette modification de l’objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c2614-105">The **RecordsetChangeComplete** event is called after the **Recordset** has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2614-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2614-106">Syntax</span></span>

<span data-ttu-id="c2614-107">WillChangeRecordset *adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="c2614-107">WillChangeRecordset *adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="c2614-108">RecordsetChangeComplete *adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="c2614-108">RecordsetChangeComplete *adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="c2614-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2614-109">Parameters</span></span>

|<span data-ttu-id="c2614-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c2614-110">Parameter</span></span>|<span data-ttu-id="c2614-111">Description</span><span class="sxs-lookup"><span data-stu-id="c2614-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c2614-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="c2614-112">*adReason*</span></span> |<span data-ttu-id="c2614-p102">Valeur [EventReasonEnum](eventreasonenum.md) indiquant la raison de cet événement. Les valeurs possibles sont **adRsnRequery**, **adRsnResynch**, **adRsnClose** et **adRsnOpen**.</span><span class="sxs-lookup"><span data-stu-id="c2614-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span></span>|
|<span data-ttu-id="c2614-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="c2614-115">*adStatus*</span></span> |<span data-ttu-id="c2614-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="c2614-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="c2614-117">Lorsque **WillChangeRecordset** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement.</span><span class="sxs-lookup"><span data-stu-id="c2614-117">When **WillChangeRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="c2614-118">Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="c2614-118">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="c2614-119">Lorsque **RecordsetChangeComplete** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement, à **adStatusErrorsOccurred** si cette dernière a échoué ou encore à **adStatusCancel** si l'opération associée à l'événement **WillChangeRecordset** précédemment accepté a été annulée</span><span class="sxs-lookup"><span data-stu-id="c2614-119">When **RecordsetChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, **adStatusErrorsOccurred** if the operation failed, or **adStatusCancel** if the operation associated with the previously accepted **WillChangeRecordset** event has been canceled.</span></span> <br/><br/><span data-ttu-id="c2614-120">Avant que **WillChangeRecordset** soit retourné, définissez ce paramètre à **adStatusCancel** pour demander l'annulation de l'opération en attente ou à adStatusUnwantedEvent pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c2614-120">Before **WillChangeRecordset** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</span></span> <br/><br/><span data-ttu-id="c2614-121">Avant que **WillChangeRecordset** ou que **RecordsetChangeComplete** soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c2614-121">Before **WillChangeRecordset** or **RecordsetChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="c2614-122">*pError*</span><span class="sxs-lookup"><span data-stu-id="c2614-122">*pError*</span></span> |<span data-ttu-id="c2614-p104">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="c2614-p104">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="c2614-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="c2614-125">*pRecordset*</span></span> |<span data-ttu-id="c2614-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span><span class="sxs-lookup"><span data-stu-id="c2614-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c2614-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2614-128">Remarks</span></span>

<span data-ttu-id="c2614-129">Un **événement WillChangeRecordset** ou **RecordsetChangeComplete** peut se produire en raison des méthodes [Requery](requery-method-ado.md) ou [Open](open-method-ado-recordset.md) du jeu d’enregistrements. </span><span class="sxs-lookup"><span data-stu-id="c2614-129">A **WillChangeRecordset** or **RecordsetChangeComplete** event may occur due to the **Recordset** [Requery](requery-method-ado.md) or [Open](open-method-ado-recordset.md) methods.</span></span>

<span data-ttu-id="c2614-p106">Si le fournisseur ne prend pas en charge les signets, une notification d'événement **RecordsetChange** est générée chaque fois que des nouvelles lignes sont extraites du fournisseur. La fréquence de cet événement dépend de la propriété **RecordsetCacheSize**.</span><span class="sxs-lookup"><span data-stu-id="c2614-p106">If the provider does not support bookmarks, a **RecordsetChange** event notification occurs each time new rows are retrieved from the provider. The frequency of this event depends on the **RecordsetCacheSize** property.</span></span>

<span data-ttu-id="c2614-132">Vous devez affecter au paramètre **adStatus** la valeur **adStatusUnwantedEvent** pour chaque valeur possible du paramètre **adReason** afin d'empêcher définitivement les notifications des événements comprenant un paramètre **adReason**.</span><span class="sxs-lookup"><span data-stu-id="c2614-132">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible **adReason** value in order to completely stop event notification for any event that includes an **adReason** parameter.</span></span>

