---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418336"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="55c5d-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55c5d-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="55c5d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55c5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55c5d-105">Transmet le fournisseur de magasin en tant que champ sur la structure MAPISIB pendant un appel à [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="55c5d-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="55c5d-106">Le fournisseur de magasin utilise cette interface pour fournir des commentaires à Microsoft Outlook sur l’état de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="55c5d-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55c5d-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="55c5d-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="55c5d-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="55c5d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="55c5d-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="55c5d-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="55c5d-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="55c5d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="55c5d-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="55c5d-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="55c5d-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="55c5d-112">Called by:</span></span>  <br/> |<span data-ttu-id="55c5d-113">Fournisseurs du Store</span><span class="sxs-lookup"><span data-stu-id="55c5d-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="55c5d-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="55c5d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="55c5d-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="55c5d-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="55c5d-116">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="55c5d-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="55c5d-117">Progress</span><span class="sxs-lookup"><span data-stu-id="55c5d-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="55c5d-118">Le fournisseur de magasins appelle régulièrement cette fonction pour mettre à jour l’état dans la boîte de dialogue d’envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="55c5d-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="55c5d-119">Error</span><span class="sxs-lookup"><span data-stu-id="55c5d-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="55c5d-120">Si des erreurs se sont rencontrées lors de la synchronisation, le fournisseur de magasins appelle cette fonction pour fournir des détails affichés dans la boîte de dialogue d’envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="55c5d-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="55c5d-121">Terminé</span><span class="sxs-lookup"><span data-stu-id="55c5d-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="55c5d-122">Le fournisseur de magasin appelle cette fonction pour informer Outlook que la synchronisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="55c5d-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55c5d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55c5d-123">See also</span></span>



[<span data-ttu-id="55c5d-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55c5d-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="55c5d-125">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="55c5d-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

