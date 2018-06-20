---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783947"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="dd834-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="dd834-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="dd834-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dd834-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dd834-105">Requêtes le fournisseur MAPI pour arrêt rapide prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="dd834-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="dd834-106">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="dd834-106">Return value</span></span>

<span data-ttu-id="dd834-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd834-107">S_OK</span></span>
  
> <span data-ttu-id="dd834-108">Le fournisseur MAPI prend en charge le client MAPI pour rapide de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="dd834-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="dd834-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="dd834-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="dd834-110">Le fournisseur MAPI ne gère pas le client MAPI pour rapide de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="dd834-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd834-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd834-111">Remarks</span></span>

<span data-ttu-id="dd834-112">Fournisseurs MAPI qui n’ont pas besoin pour prendre en charge l’arrêt rapide client doivent toujours implémenter l’interface [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) et que la méthode de **IMAPIProviderShutdown::QueryFastShutdown** renvoie MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="dd834-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="dd834-113">Pour Outlook en tant qu’un client MAPI, cela entraîne à attendre que toutes les références externes doit être publié avant de quitter Outlook.</span><span class="sxs-lookup"><span data-stu-id="dd834-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="dd834-114">Dans le Registre Windows de l’utilisateur en fonction de paramètre d’arrêt rapide, ne pas l’implémentation de l’interface **IMAPIProviderShutdown** n’empêche pas nécessairement un arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="dd834-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd834-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd834-115">See also</span></span>



[<span data-ttu-id="dd834-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd834-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="dd834-117">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="dd834-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

