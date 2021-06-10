---
title: ConnectComplete and Disconnect events (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295988"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="d9d5b-102">ConnectComplete and Disconnect events (ADO)</span><span class="sxs-lookup"><span data-stu-id="d9d5b-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="d9d5b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9d5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9d5b-p101">L'événement **ConnectComplete** est appelé après l'*établissement* d'une connexion. L'événement **Disconnect** est pour sa part appelé à la *fin* de la connexion.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-p101">The **ConnectComplete** event is called after a connection *starts*. The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d5b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9d5b-106">Syntax</span></span>

<span data-ttu-id="d9d5b-107">ConnectComplete *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="d9d5b-107">ConnectComplete *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="d9d5b-108">*Déconnecter adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="d9d5b-108">Disconnect *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="d9d5b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9d5b-109">Parameters</span></span>

|<span data-ttu-id="d9d5b-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d9d5b-110">Parameter</span></span>|<span data-ttu-id="d9d5b-111">Description</span><span class="sxs-lookup"><span data-stu-id="d9d5b-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d9d5b-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="d9d5b-112">*pError*</span></span> |<span data-ttu-id="d9d5b-p102">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="d9d5b-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="d9d5b-115">*adStatus*</span></span> |<span data-ttu-id="d9d5b-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="d9d5b-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="d9d5b-117">Lorsque **ConnectComplete** est appelé, ce paramètre est défini à **adStatusCancel** si un événement **WillConnect** a demandé l'annulation de la connexion en attente.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="d9d5b-p104">Avant qu'un de ces événements soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure. Notez toutefois que ces événements sont à nouveau générés si vous fermez et rouvrez l'objet [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d9d5b-p104">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="d9d5b-120">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="d9d5b-120">*pConnection*</span></span> |<span data-ttu-id="d9d5b-121">Objet **Connection** auquel l'événement se rapporte.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-121">The **Connection** object for which this event applies.</span></span>|

