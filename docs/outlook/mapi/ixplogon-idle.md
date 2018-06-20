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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 75607550f1d6085a670ad997238994400e08f7bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784499"
---
# <a name="ixplogonidle"></a><span data-ttu-id="efd10-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="efd10-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="efd10-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="efd10-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="efd10-105">Indique que le système est inactif, l’activation du fournisseur de transport effectuer des opérations de priorité basse.</span><span class="sxs-lookup"><span data-stu-id="efd10-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="efd10-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="efd10-106">Parameters</span></span>

 <span data-ttu-id="efd10-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="efd10-107">_ulFlags_</span></span>
  
> <span data-ttu-id="efd10-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="efd10-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="efd10-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="efd10-109">Return value</span></span>

<span data-ttu-id="efd10-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="efd10-110">S_OK</span></span> 
  
> <span data-ttu-id="efd10-111">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="efd10-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="efd10-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="efd10-112">Remarks</span></span>

<span data-ttu-id="efd10-113">Le spouleur MAPI appelle régulièrement la méthode **IXPLogon::Idle** , si vous y êtes invité, pendant les heures lorsque le système est inactif en transmettant l’indicateur XP_LOGON_SP dans l’appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) qui a ouvert la session en cours.</span><span class="sxs-lookup"><span data-stu-id="efd10-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="efd10-114">Lorsque le système est inactif, le fournisseur de transport peut effectuer des opérations en arrière-plan qui ne sont pas appropriés pendant les autres appels, ou qui ont besoin de se produire à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="efd10-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efd10-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efd10-115">See also</span></span>



[<span data-ttu-id="efd10-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="efd10-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="efd10-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="efd10-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

