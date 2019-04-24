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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350917"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="23731-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23731-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="23731-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23731-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23731-105">Implémente un objet de récepteur de notifications pour la gestion de la notification.</span><span class="sxs-lookup"><span data-stu-id="23731-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="23731-106">Un pointeur vers un objet de récepteur Advise est transmis dans un appel à la méthode **Advise** d'un fournisseur de services, le mécanisme utilisé pour s'inscrire à la notification.</span><span class="sxs-lookup"><span data-stu-id="23731-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23731-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="23731-107">Header file:</span></span>  <br/> |<span data-ttu-id="23731-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="23731-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="23731-109">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="23731-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="23731-110">Objets de récepteur de notifications</span><span class="sxs-lookup"><span data-stu-id="23731-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="23731-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="23731-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="23731-112">Applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="23731-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="23731-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="23731-113">Called by:</span></span>  <br/> |<span data-ttu-id="23731-114">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="23731-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="23731-115">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="23731-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="23731-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="23731-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="23731-117">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="23731-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="23731-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="23731-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="23731-119">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="23731-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="23731-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="23731-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="23731-121">Répond à une notification en effectuant une ou plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="23731-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="23731-122">Les tâches effectuées dépendent du type d'événement et de l'objet qui génère la notification.</span><span class="sxs-lookup"><span data-stu-id="23731-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23731-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23731-123">See also</span></span>



[<span data-ttu-id="23731-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="23731-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

