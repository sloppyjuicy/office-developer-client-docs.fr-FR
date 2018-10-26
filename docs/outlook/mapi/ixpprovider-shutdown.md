---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592604"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="f42da-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="f42da-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="f42da-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f42da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f42da-105">Ferme un fournisseur de transport de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="f42da-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f42da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f42da-106">Parameters</span></span>

 <span data-ttu-id="f42da-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="f42da-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="f42da-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="f42da-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f42da-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f42da-109">Return value</span></span>

<span data-ttu-id="f42da-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f42da-110">S_OK</span></span> 
  
> <span data-ttu-id="f42da-111">L’appel a réussi à l’arrêt du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="f42da-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f42da-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="f42da-112">Remarks</span></span>

<span data-ttu-id="f42da-113">Le spouleur MAPI appelle la méthode **IXPProvider::Shutdown** juste avant la libération d’un objet de fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="f42da-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="f42da-114">Avant d’appeler **l’arrêt**, MAPI libère tous les objets d’ouverture de session pour un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f42da-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f42da-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f42da-115">See also</span></span>



[<span data-ttu-id="f42da-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="f42da-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="f42da-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f42da-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

