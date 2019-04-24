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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298480"
---
# <a name="ixplogonidle"></a><span data-ttu-id="73c02-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="73c02-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="73c02-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73c02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73c02-105">Indique que le système est inactif, ce qui permet au fournisseur de transport d'effectuer des opérations de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="73c02-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="73c02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73c02-106">Parameters</span></span>

 <span data-ttu-id="73c02-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="73c02-107">_ulFlags_</span></span>
  
> <span data-ttu-id="73c02-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="73c02-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73c02-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="73c02-109">Return value</span></span>

<span data-ttu-id="73c02-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="73c02-110">S_OK</span></span> 
  
> <span data-ttu-id="73c02-111">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="73c02-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73c02-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="73c02-112">Remarks</span></span>

<span data-ttu-id="73c02-113">Le spouleur MAPI appelle régulièrement la méthode **IXPLogon:: Idle** , si elle est demandée, lorsque le système est inactif en transmettant l'indicateur XP_LOGON_SP dans l'appel à la méthode [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) qui a ouvert la session en cours.</span><span class="sxs-lookup"><span data-stu-id="73c02-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="73c02-114">Lorsque le système est inactif, le fournisseur de transport peut effectuer des opérations d'arrière-plan qui ne sont pas appropriées pendant les autres appels ou qui doivent se produire à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="73c02-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73c02-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73c02-115">See also</span></span>



[<span data-ttu-id="73c02-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="73c02-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="73c02-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73c02-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

