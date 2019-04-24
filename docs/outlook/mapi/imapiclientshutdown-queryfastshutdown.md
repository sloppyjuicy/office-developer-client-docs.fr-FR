---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350868"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="580f8-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="580f8-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="580f8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="580f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="580f8-105">Interroge le sous-système MAPI pour la prise en charge de l'arrêt rapide fourni par les fournisseurs MAPI chargés.</span><span class="sxs-lookup"><span data-stu-id="580f8-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="580f8-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="580f8-106">Return value</span></span>

<span data-ttu-id="580f8-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="580f8-107">S_OK</span></span>
  
> <span data-ttu-id="580f8-108">Le sous-système MAPI prend en charge le client MAPI pour l'arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="580f8-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="580f8-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="580f8-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="580f8-110">Le fournisseur MAPI ne prend pas en charge le client MAPI pour l'arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="580f8-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="580f8-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="580f8-111">Remarks</span></span>

<span data-ttu-id="580f8-112">Le fait que le sous-système MAPI prenne en charge le client MAPI pour l'arrêt rapide dépend du paramètre de Registre Windows de l'utilisateur ou du comportement par défaut du client MAPI pour l'arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="580f8-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="580f8-113">Cela dépend également de la capacité des fournisseurs MAPI chargés à prendre en charge la mise à l'arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="580f8-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="580f8-114">Pour plus d'informations, consultez la rubrique options de l' [utilisateur à arrêt rapide](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="580f8-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="580f8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="580f8-115">See also</span></span>



[<span data-ttu-id="580f8-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="580f8-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="580f8-117">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="580f8-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

