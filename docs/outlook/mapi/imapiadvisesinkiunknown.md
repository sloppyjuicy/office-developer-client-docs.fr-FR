---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409565"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="3dfef-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3dfef-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="3dfef-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dfef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dfef-105">Implémente un objet de récepteur de notifications pour la gestion de la notification.</span><span class="sxs-lookup"><span data-stu-id="3dfef-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="3dfef-106">Un pointeur vers un objet de récepteur Advise est transmis dans un appel à la méthode **Advise** d'un fournisseur de services, le mécanisme utilisé pour s'inscrire à la notification.</span><span class="sxs-lookup"><span data-stu-id="3dfef-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3dfef-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3dfef-107">Header file:</span></span>  <br/> |<span data-ttu-id="3dfef-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3dfef-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3dfef-109">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="3dfef-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="3dfef-110">Objets de récepteur de notifications</span><span class="sxs-lookup"><span data-stu-id="3dfef-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="3dfef-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="3dfef-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="3dfef-112">Applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="3dfef-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="3dfef-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="3dfef-113">Called by:</span></span>  <br/> |<span data-ttu-id="3dfef-114">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="3dfef-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="3dfef-115">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="3dfef-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3dfef-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3dfef-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="3dfef-117">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="3dfef-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="3dfef-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="3dfef-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3dfef-119">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="3dfef-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3dfef-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="3dfef-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="3dfef-121">Répond à une notification en effectuant une ou plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="3dfef-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="3dfef-122">Les tâches effectuées dépendent du type d'événement et de l'objet qui génère la notification.</span><span class="sxs-lookup"><span data-stu-id="3dfef-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3dfef-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dfef-123">See also</span></span>



[<span data-ttu-id="3dfef-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3dfef-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

