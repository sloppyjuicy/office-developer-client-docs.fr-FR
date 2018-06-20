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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783596"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="312b5-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="312b5-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="312b5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="312b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="312b5-105">Lance le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="312b5-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="312b5-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="312b5-106">Parameters</span></span>

 <span data-ttu-id="312b5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="312b5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="312b5-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="312b5-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="312b5-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="312b5-109">Return value</span></span>

<span data-ttu-id="312b5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="312b5-110">S_OK</span></span> 
  
> <span data-ttu-id="312b5-111">Le processus de fermeture de session a été lancé.</span><span class="sxs-lookup"><span data-stu-id="312b5-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="312b5-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="312b5-112">Remarks</span></span>

<span data-ttu-id="312b5-113">Le processus de déconnexion est généralement démarré lorsqu’un client appelle la méthode [IMAPISession::Logoff](imapisession-logoff.md) pour mettre fin à une session.</span><span class="sxs-lookup"><span data-stu-id="312b5-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="312b5-114">MAPI appelle ensuite la méthode **IABLogon::Logoff** de chaque fournisseur carnet d’adresses pour démarrer le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="312b5-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="312b5-115">La méthode **IABLogon::Logoff** effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="312b5-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="312b5-116">Libère tous les objets, tels que les sous-objets ou l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="312b5-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="312b5-117">Libère l’objet de prise en charge du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="312b5-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="312b5-118">Pour plus d’informations sur le processus de déconnexion de fournisseurs de carnet d’adresses, voir [Arrêt vers le bas un fournisseur de services](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="312b5-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="312b5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="312b5-119">See also</span></span>



[<span data-ttu-id="312b5-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="312b5-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="312b5-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="312b5-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

