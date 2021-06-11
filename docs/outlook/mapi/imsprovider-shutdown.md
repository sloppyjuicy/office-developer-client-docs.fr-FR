---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438623"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="43b05-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="43b05-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="43b05-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43b05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43b05-105">Ferme un fournisseur de magasins de messages de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="43b05-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="43b05-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="43b05-106">Parameters</span></span>

 <span data-ttu-id="43b05-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="43b05-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="43b05-108">[in] Réservé ; doit être un pointeur vers zéro.</span><span class="sxs-lookup"><span data-stu-id="43b05-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43b05-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="43b05-109">Return value</span></span>

<span data-ttu-id="43b05-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="43b05-110">S_OK</span></span> 
  
> <span data-ttu-id="43b05-111">L’appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="43b05-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43b05-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="43b05-112">Remarks</span></span>

<span data-ttu-id="43b05-113">MAPI appelle la **méthode IMSProvider::Shutdown** juste avant de libérer l’objet fournisseur de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="43b05-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="43b05-114">MAPI libère tous les objets d’accès pour un fournisseur avant d’appeler **l’arrêt** pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="43b05-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43b05-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43b05-115">See also</span></span>



[<span data-ttu-id="43b05-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43b05-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

