---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 12aa8b79e38320d9767a6c333cb0197ea5669862
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578010"
---
# <a name="ixplogonidle"></a><span data-ttu-id="10b9d-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="10b9d-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="10b9d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10b9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10b9d-105">Indique que le système est inactif, l’activation du fournisseur de transport effectuer des opérations de priorité basse.</span><span class="sxs-lookup"><span data-stu-id="10b9d-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="10b9d-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="10b9d-106">Parameters</span></span>

 <span data-ttu-id="10b9d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="10b9d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="10b9d-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="10b9d-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10b9d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="10b9d-109">Return value</span></span>

<span data-ttu-id="10b9d-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="10b9d-110">S_OK</span></span> 
  
> <span data-ttu-id="10b9d-111">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="10b9d-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10b9d-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="10b9d-112">Remarks</span></span>

<span data-ttu-id="10b9d-113">Le spouleur MAPI appelle régulièrement la méthode **IXPLogon::Idle** , si vous y êtes invité, pendant les heures lorsque le système est inactif en transmettant l’indicateur XP_LOGON_SP dans l’appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) qui a ouvert la session en cours.</span><span class="sxs-lookup"><span data-stu-id="10b9d-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="10b9d-114">Lorsque le système est inactif, le fournisseur de transport peut effectuer des opérations en arrière-plan qui ne sont pas appropriés pendant les autres appels, ou qui ont besoin de se produire à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="10b9d-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10b9d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10b9d-115">See also</span></span>



[<span data-ttu-id="10b9d-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="10b9d-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="10b9d-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10b9d-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

