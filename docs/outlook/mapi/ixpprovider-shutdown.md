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
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409691"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="755fa-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="755fa-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="755fa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="755fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="755fa-105">Ferme un fournisseur de transport de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="755fa-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="755fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="755fa-106">Parameters</span></span>

 <span data-ttu-id="755fa-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="755fa-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="755fa-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="755fa-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="755fa-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="755fa-109">Return value</span></span>

<span data-ttu-id="755fa-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="755fa-110">S_OK</span></span> 
  
> <span data-ttu-id="755fa-111">L’appel a réussi à arrêter le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="755fa-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="755fa-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="755fa-112">Remarks</span></span>

<span data-ttu-id="755fa-113">Lepooler MAPI appelle la méthode **IXPProvider::Shutdown** juste avant de libérer un objet fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="755fa-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="755fa-114">Avant **d’appeler l’arrêt,** MAPI libère tous les objets d’accès pour un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="755fa-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="755fa-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="755fa-115">See also</span></span>



[<span data-ttu-id="755fa-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="755fa-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="755fa-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="755fa-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

