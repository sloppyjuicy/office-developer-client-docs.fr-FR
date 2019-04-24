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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317261"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="71068-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="71068-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="71068-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71068-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71068-105">Ferme un fournisseur de banque de messages de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="71068-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="71068-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71068-106">Parameters</span></span>

 <span data-ttu-id="71068-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="71068-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="71068-108">dans MSR doit être un pointeur vers zéro.</span><span class="sxs-lookup"><span data-stu-id="71068-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="71068-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71068-109">Return value</span></span>

<span data-ttu-id="71068-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="71068-110">S_OK</span></span> 
  
> <span data-ttu-id="71068-111">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="71068-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="71068-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="71068-112">Remarks</span></span>

<span data-ttu-id="71068-113">MAPI appelle la méthode **IMSProvider:: Shutdown** juste avant de libérer l'objet fournisseur de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="71068-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="71068-114">MAPI libère tous les objets d'ouverture de session pour un fournisseur avant d'appeler l' **arrêt** pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71068-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="71068-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71068-115">See also</span></span>



[<span data-ttu-id="71068-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71068-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

