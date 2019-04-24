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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341236"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="8b2e7-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b2e7-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="8b2e7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b2e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b2e7-105">Transmet le fournisseur Store en tant que champ sur la structure MAPISIB lors d'un appel à [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="8b2e7-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="8b2e7-106">Le fournisseur de banque d'informations utilise cette interface pour envoyer des commentaires à Microsoft Outlook sur l'état de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b2e7-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8b2e7-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="8b2e7-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="8b2e7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8b2e7-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="8b2e7-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="8b2e7-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8b2e7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8b2e7-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="8b2e7-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="8b2e7-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8b2e7-112">Called by:</span></span>  <br/> |<span data-ttu-id="8b2e7-113">Fournisseurs de magasin</span><span class="sxs-lookup"><span data-stu-id="8b2e7-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="8b2e7-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="8b2e7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8b2e7-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="8b2e7-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8b2e7-116">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="8b2e7-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8b2e7-117">Progress</span><span class="sxs-lookup"><span data-stu-id="8b2e7-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="8b2e7-118">Le fournisseur Store appelle régulièrement cette fonction pour mettre à jour l'État dans la boîte de dialogue d'envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="8b2e7-119">Error</span><span class="sxs-lookup"><span data-stu-id="8b2e7-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="8b2e7-120">Si des erreurs se produisent lors de la synchronisation, le fournisseur de banque d'informations appelle cette fonction pour fournir les détails affichés dans la boîte de dialogue d'envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="8b2e7-121">Terminé</span><span class="sxs-lookup"><span data-stu-id="8b2e7-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="8b2e7-122">Le fournisseur Store appelle cette fonction pour informer Outlook que la synchronisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b2e7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b2e7-123">See also</span></span>



[<span data-ttu-id="8b2e7-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b2e7-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="8b2e7-125">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8b2e7-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

