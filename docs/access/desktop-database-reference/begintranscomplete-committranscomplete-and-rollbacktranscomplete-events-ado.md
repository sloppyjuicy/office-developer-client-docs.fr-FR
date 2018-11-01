---
title: BeginTransComplete, CommitTransComplete, RollbackTransComplete, événements (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf38a106a8cb53c1603628f0c3c0096be4b73d52
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888635"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="9b588-102">BeginTransComplete, CommitTransComplete et RollbackTransComplete, événements (ADO)</span><span class="sxs-lookup"><span data-stu-id="9b588-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)</span></span>


<span data-ttu-id="9b588-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b588-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="9b588-104">Ces événements sont appelés une fois l'opération associée à l'objet [Connection](connection-object-ado.md) terminée.</span><span class="sxs-lookup"><span data-stu-id="9b588-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

  - <span data-ttu-id="9b588-105">**BeginTransComplete** est appelé après l'opération [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9b588-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="9b588-106">**CommitTransComplete** est appelé après l'opération [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9b588-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="9b588-107">**RollbackTransComplete** est appelé après l'opération [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9b588-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b588-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b588-108">Syntax</span></span>

<span data-ttu-id="9b588-109">De le BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="9b588-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="9b588-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="9b588-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="9b588-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="9b588-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="9b588-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b588-112">Parameters</span></span>

  - <span data-ttu-id="9b588-113">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="9b588-113">*TransactionLevel*</span></span>

  - <span data-ttu-id="9b588-114">Valeur de type **Long** contenant le nouveau niveau de transaction de l'événement **BeginTrans** qui a provoqué l'événement.</span><span class="sxs-lookup"><span data-stu-id="9b588-114">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>

  - <span data-ttu-id="9b588-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="9b588-115">*pError*</span></span>

  - <span data-ttu-id="9b588-p101">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si EventStatusEnum a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="9b588-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="9b588-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="9b588-118">*adStatus*</span></span>

  - [<span data-ttu-id="9b588-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="9b588-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="9b588-120">Ces événements peuvent empêcher la génération de notifications ultérieures en définissant ce paramètre à **adStatusUnwantedEvent** avant que l'événement soit retourné.</span><span class="sxs-lookup"><span data-stu-id="9b588-120">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>

  - <span data-ttu-id="9b588-121">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="9b588-121">*pConnection*</span></span>

  - <span data-ttu-id="9b588-122">Objet **Connection** pour lequel l'événement s'est produit.</span><span class="sxs-lookup"><span data-stu-id="9b588-122">The **Connection** object for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b588-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9b588-123">Remarks</span></span>

<span data-ttu-id="9b588-p102">En Visual C++, plusieurs objets **Connection** peuvent partager la même méthode de gestion des événements. Celle-ci utilise l'objet **Connection** retourné pour identifier l'objet à l'origine de l'événement.</span><span class="sxs-lookup"><span data-stu-id="9b588-p102">In Visual C++, multiple **Connections** can share the same event handling method. The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="9b588-p103">Si la propriété [Attributes](attributes-property-ado.md) a la valeur **adXactCommitRetaining** ou **adXactAbortRetaining**, une nouvelle transaction est lancée après la validation ou la restauration d'une transaction. Utilisez l'événement **BeginTransComplete** pour ignorer tous les événements de début de transaction à l'exception du premier.</span><span class="sxs-lookup"><span data-stu-id="9b588-p103">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction. Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

