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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784501"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="14788-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="14788-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="14788-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14788-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14788-105">Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants.</span><span class="sxs-lookup"><span data-stu-id="14788-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="14788-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14788-106">Parameters</span></span>

 <span data-ttu-id="14788-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="14788-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="14788-108">[out] Une valeur qui indique la présence de messages entrants.</span><span class="sxs-lookup"><span data-stu-id="14788-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="14788-109">Une valeur différente de zéro indique qu’il existe des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="14788-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14788-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="14788-110">Return value</span></span>

<span data-ttu-id="14788-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="14788-111">S_OK</span></span> 
  
> <span data-ttu-id="14788-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="14788-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14788-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="14788-113">Remarks</span></span>

<span data-ttu-id="14788-114">Le spouleur MAPI appelle régulièrement la méthode **IXPLogon::Poll** si le fournisseur de transport indique qu’il doit être interrogé pour les nouveaux messages, lequel le fournisseur signale à l’appel à [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) en transmettant le LOGON_SP_POLL méthode au début d’une session.</span><span class="sxs-lookup"><span data-stu-id="14788-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="14788-115">Si le fournisseur de transport indique en réponse à l’appel de **sondage** qu’il y a un ou plus des messages entrants disponibles pour ce processus, le spouleur MAPI appelle la méthode [IXPLogon::StartMessage](ixplogon-startmessage.md) pour autoriser le fournisseur au processus de la première entrant Message.</span><span class="sxs-lookup"><span data-stu-id="14788-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="14788-116">Le fournisseur de transport indique les messages entrants en définissant la valeur dans le paramètre _lpulIncoming_ sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="14788-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14788-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14788-117">See also</span></span>



[<span data-ttu-id="14788-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="14788-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="14788-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="14788-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="14788-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14788-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

