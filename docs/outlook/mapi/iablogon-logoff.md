---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416397"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="dd6ac-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="dd6ac-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="dd6ac-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd6ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd6ac-105">Lance le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="dd6ac-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dd6ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd6ac-106">Parameters</span></span>

 <span data-ttu-id="dd6ac-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd6ac-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dd6ac-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="dd6ac-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd6ac-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dd6ac-109">Return value</span></span>

<span data-ttu-id="dd6ac-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd6ac-110">S_OK</span></span> 
  
> <span data-ttu-id="dd6ac-111">Le processus de fermeture de session a été initié avec succès.</span><span class="sxs-lookup"><span data-stu-id="dd6ac-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd6ac-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd6ac-112">Remarks</span></span>

<span data-ttu-id="dd6ac-113">Le processus de déconnexion est généralement démarré lorsqu'un client appelle la méthode [IMAPISession:: Logoff](imapisession-logoff.md) pour mettre fin à une session.</span><span class="sxs-lookup"><span data-stu-id="dd6ac-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="dd6ac-114">MAPI appelle ensuite la méthode **IABLogon:: Logoff** du fournisseur de carnets d'adresses pour démarrer le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="dd6ac-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="dd6ac-115">La méthode **IABLogon:: Logoff** effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="dd6ac-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="dd6ac-116">Libère tous les objets ouverts, tels que les sous-objets ou l'objet d'État.</span><span class="sxs-lookup"><span data-stu-id="dd6ac-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="dd6ac-117">Libère l'objet de prise en charge du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="dd6ac-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="dd6ac-118">Pour plus d'informations sur le processus de fermeture de session des fournisseurs de carnets d'adresses, consultez la rubrique [arrêt d'un fournisseur de services](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="dd6ac-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dd6ac-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd6ac-119">See also</span></span>



[<span data-ttu-id="dd6ac-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="dd6ac-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="dd6ac-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd6ac-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

