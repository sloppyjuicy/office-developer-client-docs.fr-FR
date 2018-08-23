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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 33d811af0fc9e06902750075ba39bfb6ca88903f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593710"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="072f5-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="072f5-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="072f5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="072f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="072f5-105">Transmet le fournisseur de banque comme un champ de la structure MAPISIB pendant un appel à [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="072f5-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="072f5-106">Le fournisseur de banque utilise cette interface pour fournir des commentaires à Microsoft Outlook sur l’état de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="072f5-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="072f5-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="072f5-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="072f5-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="072f5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="072f5-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="072f5-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="072f5-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="072f5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="072f5-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="072f5-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="072f5-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="072f5-112">Called by:</span></span>  <br/> |<span data-ttu-id="072f5-113">Fournisseurs de magasins</span><span class="sxs-lookup"><span data-stu-id="072f5-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="072f5-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="072f5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="072f5-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="072f5-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="072f5-116">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="072f5-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="072f5-117">Progress</span><span class="sxs-lookup"><span data-stu-id="072f5-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="072f5-118">Le fournisseur de banque appelle régulièrement cette fonction pour mettre à jour l’état dans la boîte de dialogue d’envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="072f5-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="072f5-119">Erreur</span><span class="sxs-lookup"><span data-stu-id="072f5-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="072f5-120">Si vous rencontrez des erreurs lors de la synchronisation, le fournisseur de banque appelle cette fonction pour fournir plus d’informations qui sont affichent dans la boîte de dialogue d’envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="072f5-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="072f5-121">Terminé</span><span class="sxs-lookup"><span data-stu-id="072f5-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="072f5-122">Le fournisseur de banque appelle cette fonction pour informer Outlook que la synchronisation est terminé.</span><span class="sxs-lookup"><span data-stu-id="072f5-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="072f5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="072f5-123">See also</span></span>



[<span data-ttu-id="072f5-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="072f5-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="072f5-125">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="072f5-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

