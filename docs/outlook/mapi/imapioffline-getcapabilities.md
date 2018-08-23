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
ms.openlocfilehash: 699e77479e0d09e7549c0d2741d5ba54ecc8ce33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572031"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="753be-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="753be-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="753be-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="753be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="753be-105">Obtient les conditions pour lequel les rappels sont pris en charge par un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="753be-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="753be-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="753be-106">Parameters</span></span>

 <span data-ttu-id="753be-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="753be-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="753be-108">[out] Un masque de bits des indicateurs de capacité suivants :</span><span class="sxs-lookup"><span data-stu-id="753be-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="753be-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="753be-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="753be-110">L’objet en mode hors connexion est capable de fournir des notifications en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="753be-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="753be-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="753be-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="753be-112">L’objet en mode hors connexion est capable de fournir des notifications en ligne.</span><span class="sxs-lookup"><span data-stu-id="753be-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="753be-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="753be-113">Remarks</span></span>

<span data-ttu-id="753be-114">À l’ouverture d’un objet en mode hors connexion à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client peut interroger sur [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) pour obtenir un pointeur vers une interface **IMAPIOffline** et **IMAPIOffline::GetCapabilities** pour découvrir les rappels pris en charge des appels par l’objet.</span><span class="sxs-lookup"><span data-stu-id="753be-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="753be-115">Le client peut ensuite choisir configurer des rappels à l’aide de **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="753be-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="753be-116">Notez que, selon le serveur de messagerie pour un objet en mode hors connexion, un objet qui prend en charge des rappels pour passer en ligne ne prend pas nécessairement en charge des rappels pour passer en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="753be-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="753be-117">Notez également que, pendant un objet en mode hors connexion peut prendre en charge des rappels pour que les modifications qu’en ligne/hors connexion, l’API d’état en mode hors connexion prend en charge uniquement les modifications en ligne/hors connexion et les clients doivent vérifier pour seulement ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="753be-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="753be-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="753be-118">See also</span></span>



[<span data-ttu-id="753be-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="753be-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="753be-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="753be-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="753be-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="753be-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="753be-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="753be-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="753be-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="753be-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

