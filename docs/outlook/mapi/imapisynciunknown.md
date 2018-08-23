---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8e2e7a3f9279485d862fac5bb6413b3d3eb1343e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589083"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="a1419-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1419-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="a1419-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1419-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1419-105">Fournit un mécanisme de synchronisation de messagerie au lieu d’utiliser l’API de Transport.</span><span class="sxs-lookup"><span data-stu-id="a1419-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="a1419-106">Cette interface est exposée sur un objet store.</span><span class="sxs-lookup"><span data-stu-id="a1419-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="a1419-107">À l’aide de cette interface et [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), un fournisseur de transport peut fournir une meilleure progression et messages d’erreur que celles qui s’affichent dans la boîte de dialogue d’envoi/réception dans Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="a1419-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="a1419-108">La boîte d’envoi est toujours dans la banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="a1419-108">The outbox is still in the default store.</span></span> <span data-ttu-id="a1419-109">Outlook continuera à utiliser les API de Transport pour envoyer du courrier électronique, car le message sortant ne peut pas être dans le magasin externe.</span><span class="sxs-lookup"><span data-stu-id="a1419-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1419-110">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="a1419-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="a1419-111">Fournisseurs de banque et de transport</span><span class="sxs-lookup"><span data-stu-id="a1419-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="a1419-112">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a1419-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1419-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="a1419-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="a1419-114">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="a1419-114">Called by:</span></span>  <br/> |<span data-ttu-id="a1419-115">Fournisseurs de banque et de Transport</span><span class="sxs-lookup"><span data-stu-id="a1419-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="a1419-116">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="a1419-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a1419-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="a1419-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a1419-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="a1419-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a1419-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="a1419-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="a1419-120">Implémenté par les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="a1419-120">Implemented by message store providers.</span></span> <span data-ttu-id="a1419-121">Cette méthode est appelée par Outlook 2010 et Outlook 2013 pour démarrer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="a1419-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1419-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1419-122">See also</span></span>



[<span data-ttu-id="a1419-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1419-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="a1419-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a1419-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

