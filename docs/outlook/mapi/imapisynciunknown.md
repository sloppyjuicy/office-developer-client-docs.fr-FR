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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405590"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="1bad2-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1bad2-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="1bad2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bad2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bad2-105">Fournit un mécanisme de synchronisation du courrier électronique au lieu d’utiliser l’API de transport.</span><span class="sxs-lookup"><span data-stu-id="1bad2-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="1bad2-106">Cette interface est exposée sur un objet store.</span><span class="sxs-lookup"><span data-stu-id="1bad2-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="1bad2-107">À l’aide de cette interface et [de IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), un fournisseur de transport peut fournir des messages d’erreur et de progression meilleurs que ceux qui apparaissent dans la boîte de dialogue d’envoi/réception dans Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="1bad2-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="1bad2-108">La boîte d’envoi se trouve toujours dans le magasin par défaut.</span><span class="sxs-lookup"><span data-stu-id="1bad2-108">The outbox is still in the default store.</span></span> <span data-ttu-id="1bad2-109">Outlook continuera à utiliser les API de transport pour envoyer des messages, car le message sortant ne peut pas se trouver dans le magasin externe.</span><span class="sxs-lookup"><span data-stu-id="1bad2-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1bad2-110">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="1bad2-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="1bad2-111">Fournisseurs de transport et de magasin</span><span class="sxs-lookup"><span data-stu-id="1bad2-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="1bad2-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="1bad2-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="1bad2-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="1bad2-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="1bad2-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="1bad2-114">Called by:</span></span>  <br/> |<span data-ttu-id="1bad2-115">Fournisseurs de magasins et de transports</span><span class="sxs-lookup"><span data-stu-id="1bad2-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="1bad2-116">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="1bad2-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1bad2-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="1bad2-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1bad2-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="1bad2-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1bad2-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="1bad2-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="1bad2-120">Implémenté par les fournisseurs de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="1bad2-120">Implemented by message store providers.</span></span> <span data-ttu-id="1bad2-121">Cette méthode est appelée par Outlook 2010 et Outlook 2013 pour démarrer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="1bad2-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bad2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bad2-122">See also</span></span>



[<span data-ttu-id="1bad2-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1bad2-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="1bad2-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="1bad2-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

