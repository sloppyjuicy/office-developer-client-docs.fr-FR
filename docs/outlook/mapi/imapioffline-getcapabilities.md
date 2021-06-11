---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433373"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="3375e-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="3375e-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="3375e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3375e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3375e-105">Obtient les conditions pour lesquelles les rappels sont pris en charge par un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3375e-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="3375e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3375e-106">Parameters</span></span>

 <span data-ttu-id="3375e-107">_OleCapablities_</span><span class="sxs-lookup"><span data-stu-id="3375e-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="3375e-108">[out] Masque de bits des indicateurs de fonctionnalité suivants :</span><span class="sxs-lookup"><span data-stu-id="3375e-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="3375e-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="3375e-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="3375e-110">L’objet hors connexion est capable de fournir des notifications hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3375e-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="3375e-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="3375e-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="3375e-112">L’objet hors connexion est capable de fournir des notifications en ligne.</span><span class="sxs-lookup"><span data-stu-id="3375e-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3375e-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="3375e-113">Remarks</span></span>

<span data-ttu-id="3375e-114">Lors de l’ouverture d’un objet hors connexion à l’aide de **[HrOpenOfflineObj,](hropenofflineobj.md)** un client peut interroger [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) pour obtenir un pointeur vers une interface **IMAPIOffline** et appeler **IMAPIOffline::GetCapabilities** pour rechercher les rappels pris en charge par l’objet.</span><span class="sxs-lookup"><span data-stu-id="3375e-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="3375e-115">Le client peut ensuite choisir de configurer des rappels à l’aide **d’IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="3375e-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="3375e-116">Notez que, selon le serveur de messagerie d’un objet hors connexion, un objet qui prend en charge les rappels pour la mise en ligne ne prend pas nécessairement en charge les rappels pour la mise hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3375e-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="3375e-117">Notez également que, bien qu’un objet hors connexion puisse prendre en charge les rappels pour les modifications autres que celles en ligne/hors connexion, l’API d’état hors connexion prend uniquement en charge les modifications en ligne/hors connexion, et les clients doivent vérifier uniquement ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="3375e-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3375e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3375e-118">See also</span></span>



[<span data-ttu-id="3375e-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="3375e-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="3375e-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="3375e-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="3375e-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="3375e-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="3375e-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3375e-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3375e-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="3375e-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

