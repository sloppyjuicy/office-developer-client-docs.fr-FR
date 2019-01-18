---
title: WillConnect, événement (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e62a01d274752b33f7bf3f6f4af6171e7efb16b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703432"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="69bbb-102">WillConnect, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="69bbb-102">WillConnect event (ADO)</span></span>

<span data-ttu-id="69bbb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69bbb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69bbb-104">L'événement **WillConnect** est appelé avant le début d'une connexion.</span><span class="sxs-lookup"><span data-stu-id="69bbb-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="69bbb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69bbb-105">Syntax</span></span>

<span data-ttu-id="69bbb-106">WillConnect*ConnectionString*, *UserID*, *le mot de passe*, *Options*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="69bbb-106">WillConnect*ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="69bbb-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="69bbb-107">Parameters</span></span>

|<span data-ttu-id="69bbb-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="69bbb-108">Parameter</span></span>|<span data-ttu-id="69bbb-109">Description</span><span class="sxs-lookup"><span data-stu-id="69bbb-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="69bbb-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="69bbb-110">*ConnectionString*</span></span> |<span data-ttu-id="69bbb-111">Valeur de type **String** contenant les informations de la connexion en attente.</span><span class="sxs-lookup"><span data-stu-id="69bbb-111">A **String** that contains connection information for the pending connection.</span></span>|
|<span data-ttu-id="69bbb-112">*UserID*</span><span class="sxs-lookup"><span data-stu-id="69bbb-112">*UserID*</span></span> |<span data-ttu-id="69bbb-113">Valeur de type **String** reprenant le nom de l'utilisateur de la connexion en attente.</span><span class="sxs-lookup"><span data-stu-id="69bbb-113">A **String** that contains a user name for the pending connection.</span></span>|
|<span data-ttu-id="69bbb-114">*Password*</span><span class="sxs-lookup"><span data-stu-id="69bbb-114">*Password*</span></span> |<span data-ttu-id="69bbb-115">Valeur de type **String** contenant un mot de passe pour la connexion en attente.</span><span class="sxs-lookup"><span data-stu-id="69bbb-115">A **String** that contains a password for the pending connection.</span></span>|
|<span data-ttu-id="69bbb-116">*Options*</span><span class="sxs-lookup"><span data-stu-id="69bbb-116">*Options*</span></span> |<span data-ttu-id="69bbb-p101">Valeur de type **Long** indiquant la méthode d'évaluation du paramètre *ConnectionString* par le fournisseur. La seule option possible est **adAsyncOpen**.</span><span class="sxs-lookup"><span data-stu-id="69bbb-p101">A **Long** value that indicates how the provider should evaluate the *ConnectionString*. Your only option is **adAsyncOpen**.</span></span>|
|<span data-ttu-id="69bbb-119">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="69bbb-119">*adStatus*</span></span> |<span data-ttu-id="69bbb-120">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="69bbb-120">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="69bbb-121">Lorsque cet événement est appelé, ce paramètre est défini à **adStatusOK** par défaut.</span><span class="sxs-lookup"><span data-stu-id="69bbb-121">When this event is called, this parameter is set to **adStatusOK** by default.</span></span> <span data-ttu-id="69bbb-122">Il est défini à **adStatusCantDeny** si l'événement ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="69bbb-122">It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span><br/><br/><span data-ttu-id="69bbb-p103">Avant que cet événement soit retourné, affectez au paramètre la valeur **adStatusUnwantedEvent** pour éviter toute notification ultérieure ou la valeur **adStatusCancel** pour demander l'opération de connexion provoquant l'annulation de cette notification.</span><span class="sxs-lookup"><span data-stu-id="69bbb-p103">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>|
|<span data-ttu-id="69bbb-125">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="69bbb-125">*pConnection*</span></span> |<span data-ttu-id="69bbb-p104">Objet [Connection](connection-object-ado.md) auquel cette notification d'événement s'applique. Les modifications apportées aux paramètres de l'objet **Connection** par le gestionnaire d'événements **WillConnect** n'ont aucun effet sur l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="69bbb-p104">The [Connection](connection-object-ado.md) object for which this event notification applies. Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="69bbb-128">Notes</span><span class="sxs-lookup"><span data-stu-id="69bbb-128">Remarks</span></span>

<span data-ttu-id="69bbb-p105">Si **WillConnect** est appelé, les paramètres *ConnectionString*, *UserID*, *Password* et *Options* prennent les valeurs établies par l'opération à l'origine de l'événement (à savoir, la connexion en attente) et ne peuvent pas être modifiés tant que l'événement n'est pas retourné. Il se peut que le gestionnaire d'événements **WillConnect** renvoie une demande d'annulation de la connexion en attente.</span><span class="sxs-lookup"><span data-stu-id="69bbb-p105">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns. **WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="69bbb-131">Lorsque cet événement est annulé, **ConnectComplete** est alors appelé et son paramètre *adStatus* la valeur **adStatusErrorsOccurred**.</span><span class="sxs-lookup"><span data-stu-id="69bbb-131">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>

