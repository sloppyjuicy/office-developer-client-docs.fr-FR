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
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589090"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="36d15-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="36d15-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="36d15-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36d15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36d15-105">Ferme un fournisseur de magasin de message de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="36d15-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="36d15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36d15-106">Parameters</span></span>

 <span data-ttu-id="36d15-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="36d15-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="36d15-108">[in] Réservé ; doit être un pointeur vers zéro.</span><span class="sxs-lookup"><span data-stu-id="36d15-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36d15-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="36d15-109">Return value</span></span>

<span data-ttu-id="36d15-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="36d15-110">S_OK</span></span> 
  
> <span data-ttu-id="36d15-111">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="36d15-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36d15-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="36d15-112">Remarks</span></span>

<span data-ttu-id="36d15-113">MAPI appelle la méthode **IMSProvider::Shutdown** juste avant de libérer l’objet de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="36d15-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="36d15-114">MAPI libère tous les objets d’ouverture de session pour un fournisseur avant l’appel de **l’arrêt** de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="36d15-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36d15-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36d15-115">See also</span></span>



[<span data-ttu-id="36d15-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36d15-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

