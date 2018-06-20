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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 059d0d4427a8f2d68795a671d77fb9e3d84294f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783709"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="6f123-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="6f123-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="6f123-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f123-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f123-105">Requêtes du sous-système MAPI pour arrêt rapide prennent en charge fournie par les fournisseurs MAPI chargés.</span><span class="sxs-lookup"><span data-stu-id="6f123-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="6f123-106">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6f123-106">Return value</span></span>

<span data-ttu-id="6f123-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f123-107">S_OK</span></span>
  
> <span data-ttu-id="6f123-108">Le sous-système MAPI prend en charge le client MAPI pour rapide de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="6f123-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="6f123-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6f123-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="6f123-110">Le fournisseur MAPI ne gère pas le client MAPI pour rapide de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="6f123-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f123-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f123-111">Remarks</span></span>

<span data-ttu-id="6f123-112">Si le sous-système MAPI prend en charge le client MAPI à rapide d’arrêt dépend du paramètre de Registre Windows de l’utilisateur ou le comportement par défaut du client MAPI pour l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="6f123-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="6f123-113">Cela dépend également la possibilité des fournisseurs MAPI chargés pour prendre en charge l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="6f123-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="6f123-114">Pour plus d’informations, voir [Options d’utilisateur de l’arrêt rapide](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="6f123-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6f123-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f123-115">See also</span></span>



[<span data-ttu-id="6f123-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6f123-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="6f123-117">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="6f123-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

