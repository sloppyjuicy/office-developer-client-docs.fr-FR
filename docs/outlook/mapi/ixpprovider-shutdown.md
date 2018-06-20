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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f5d253d0306e55699fbe5b9c9decf8c3242867fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784510"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="1687a-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="1687a-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="1687a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1687a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1687a-105">Ferme un fournisseur de transport de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="1687a-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1687a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1687a-106">Parameters</span></span>

 <span data-ttu-id="1687a-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="1687a-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="1687a-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="1687a-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1687a-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1687a-109">Return value</span></span>

<span data-ttu-id="1687a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1687a-110">S_OK</span></span> 
  
> <span data-ttu-id="1687a-111">L’appel a réussi à l’arrêt du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="1687a-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1687a-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="1687a-112">Remarks</span></span>

<span data-ttu-id="1687a-113">Le spouleur MAPI appelle la méthode **IXPProvider::Shutdown** juste avant la libération d’un objet de fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="1687a-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="1687a-114">Avant d’appeler **l’arrêt**, MAPI libère tous les objets d’ouverture de session pour un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1687a-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1687a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1687a-115">See also</span></span>



[<span data-ttu-id="1687a-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="1687a-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="1687a-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1687a-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

