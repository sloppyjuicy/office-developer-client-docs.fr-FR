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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fb7a8ea39d6e7b1d7df1560658ceb67a79d39d92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784053"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="d67c4-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d67c4-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="d67c4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d67c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d67c4-105">Fournit un mécanisme de synchronisation de messagerie au lieu d’utiliser l’API de Transport.</span><span class="sxs-lookup"><span data-stu-id="d67c4-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="d67c4-106">Cette interface est exposée sur un objet store.</span><span class="sxs-lookup"><span data-stu-id="d67c4-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="d67c4-107">À l’aide de cette interface et [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), un fournisseur de transport peut fournir une meilleure progression et messages d’erreur que celles qui s’affichent dans la boîte de dialogue d’envoi/réception dans Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="d67c4-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="d67c4-108">La boîte d’envoi est toujours dans la banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="d67c4-108">The outbox is still in the default store.</span></span> <span data-ttu-id="d67c4-109">Outlook continuera à utiliser les API de Transport pour envoyer du courrier électronique, car le message sortant ne peut pas être dans le magasin externe.</span><span class="sxs-lookup"><span data-stu-id="d67c4-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d67c4-110">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="d67c4-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="d67c4-111">Fournisseurs de banque et de transport</span><span class="sxs-lookup"><span data-stu-id="d67c4-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="d67c4-112">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="d67c4-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="d67c4-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="d67c4-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="d67c4-114">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="d67c4-114">Called by:</span></span>  <br/> |<span data-ttu-id="d67c4-115">Fournisseurs de banque et de Transport</span><span class="sxs-lookup"><span data-stu-id="d67c4-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="d67c4-116">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="d67c4-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d67c4-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="d67c4-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d67c4-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="d67c4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d67c4-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="d67c4-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="d67c4-120">Implémenté par les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d67c4-120">Implemented by message store providers.</span></span> <span data-ttu-id="d67c4-121">Cette méthode est appelée par Outlook 2010 et Outlook 2013 pour démarrer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="d67c4-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d67c4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d67c4-122">See also</span></span>



[<span data-ttu-id="d67c4-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d67c4-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="d67c4-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="d67c4-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

