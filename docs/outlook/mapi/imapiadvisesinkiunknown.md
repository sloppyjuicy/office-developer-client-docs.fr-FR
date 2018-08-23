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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b9244e28337c74487562ec235f246559a49a390d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573802"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="a0e5c-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0e5c-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="a0e5c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0e5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0e5c-105">Implémente un objet de récepteur advise pour la gestion des notifications.</span><span class="sxs-lookup"><span data-stu-id="a0e5c-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="a0e5c-106">Un pointeur vers un objet de récepteur advise est passé à un appel à la méthode **Advise** d’un fournisseur de service, le mécanisme utilisé pour l’enregistrement d’une notification.</span><span class="sxs-lookup"><span data-stu-id="a0e5c-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0e5c-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a0e5c-107">Header file:</span></span>  <br/> |<span data-ttu-id="a0e5c-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0e5c-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a0e5c-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="a0e5c-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a0e5c-110">Objets de récepteur de notification</span><span class="sxs-lookup"><span data-stu-id="a0e5c-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="a0e5c-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a0e5c-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a0e5c-112">Les applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="a0e5c-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="a0e5c-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="a0e5c-113">Called by:</span></span>  <br/> |<span data-ttu-id="a0e5c-114">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="a0e5c-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="a0e5c-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="a0e5c-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a0e5c-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="a0e5c-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="a0e5c-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="a0e5c-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a0e5c-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="a0e5c-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a0e5c-119">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="a0e5c-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a0e5c-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="a0e5c-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="a0e5c-121">Répond à une notification en effectuant une ou plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="a0e5c-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="a0e5c-122">Les tâches exécutées varient selon le type d’événement et l’objet qui génère la notification.</span><span class="sxs-lookup"><span data-stu-id="a0e5c-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0e5c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0e5c-123">See also</span></span>



[<span data-ttu-id="a0e5c-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a0e5c-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

