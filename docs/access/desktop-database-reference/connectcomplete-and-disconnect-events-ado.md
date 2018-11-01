---
title: ConnectComplete et Disconnect, événements (ADO)
TOCTitle: ConnectComplete and Disconnect Events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9233ba547ecf746d3b4db7b4e008976a813afff
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891182"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="6b1f5-102">ConnectComplete et Disconnect, événements (ADO)</span><span class="sxs-lookup"><span data-stu-id="6b1f5-102">ConnectComplete and Disconnect Events (ADO)</span></span>


<span data-ttu-id="6b1f5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b1f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b1f5-p101">L'événement **ConnectComplete** est appelé après l'*établissement* d'une connexion. L'événement **Disconnect** est pour sa part appelé à la *fin* de la connexion.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-p101">The **ConnectComplete** event is called after a connection *starts*. The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b1f5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b1f5-106">Syntax</span></span>

<span data-ttu-id="6b1f5-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="6b1f5-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="6b1f5-108">Déconnecter*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="6b1f5-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="6b1f5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b1f5-109">Parameters</span></span>

  - <span data-ttu-id="6b1f5-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="6b1f5-110">*pError*</span></span>

  - <span data-ttu-id="6b1f5-p102">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="6b1f5-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="6b1f5-113">*adStatus*</span></span>

  - [<span data-ttu-id="6b1f5-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="6b1f5-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="6b1f5-115">Lorsque **ConnectComplete** est appelé, ce paramètre est défini à **adStatusCancel** si un événement **WillConnect** a demandé l'annulation de la connexion en attente.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="6b1f5-p103">Avant qu'un de ces événements soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure. Notez toutefois que ces événements sont à nouveau générés si vous fermez et rouvrez l'objet [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6b1f5-p103">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

  - <span data-ttu-id="6b1f5-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="6b1f5-118">*pConnection*</span></span>

  - <span data-ttu-id="6b1f5-119">Objet **Connection** auquel l'événement se rapporte.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-119">The **Connection** object for which this event applies.</span></span>

