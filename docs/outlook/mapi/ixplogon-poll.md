---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425273"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="4f7f4-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="4f7f4-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="4f7f4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f7f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f7f4-105">Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants.</span><span class="sxs-lookup"><span data-stu-id="4f7f4-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="4f7f4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f7f4-106">Parameters</span></span>

 <span data-ttu-id="4f7f4-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="4f7f4-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="4f7f4-108">remarquer Valeur qui indique l'existence de messages entrants.</span><span class="sxs-lookup"><span data-stu-id="4f7f4-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="4f7f4-109">Une valeur non nulle indique qu'il existe des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="4f7f4-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f7f4-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4f7f4-110">Return value</span></span>

<span data-ttu-id="4f7f4-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f7f4-111">S_OK</span></span> 
  
> <span data-ttu-id="4f7f4-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4f7f4-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f7f4-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="4f7f4-113">Remarks</span></span>

<span data-ttu-id="4f7f4-114">Le spouleur MAPI appelle régulièrement la méthode **IXPLogon::P oll** si le fournisseur de transport indique qu'il doit être interrogé pour de nouveaux messages, ce que fait le fournisseur en transmettant l'indicateur LOGON_SP_POLL à l'appel à l' [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) méthode au début d'une session.</span><span class="sxs-lookup"><span data-stu-id="4f7f4-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="4f7f4-115">Si le fournisseur de transport indique en réponse à l'appel de **sondage** qu'il existe un ou plusieurs messages entrants qu'il est possible de traiter, le spouleur MAPI appelle la méthode [IXPLogon:: StartMessage](ixplogon-startmessage.md) pour permettre au fournisseur de traiter le premier Message.</span><span class="sxs-lookup"><span data-stu-id="4f7f4-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="4f7f4-116">Le fournisseur de transport indique les messages entrants en définissant la valeur du paramètre _lpulIncoming_ sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="4f7f4-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f7f4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f7f4-117">See also</span></span>



[<span data-ttu-id="4f7f4-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="4f7f4-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="4f7f4-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="4f7f4-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="4f7f4-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f7f4-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

