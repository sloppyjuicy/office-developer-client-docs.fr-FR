---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3df5e012867623d1c5e8fb5c3c93103548ab97be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588383"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="af6ea-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="af6ea-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="af6ea-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af6ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af6ea-105">Crée un récepteur de notifications qui encapsule un récepteur de notifications existant pour la sécurité des threads.</span><span class="sxs-lookup"><span data-stu-id="af6ea-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af6ea-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="af6ea-106">Header file:</span></span>  <br/> |<span data-ttu-id="af6ea-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="af6ea-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="af6ea-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="af6ea-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="af6ea-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="af6ea-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="af6ea-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="af6ea-110">Called by:</span></span>  <br/> |<span data-ttu-id="af6ea-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="af6ea-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="af6ea-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af6ea-112">Parameters</span></span>

 <span data-ttu-id="af6ea-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="af6ea-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="af6ea-114">[in] Pointeur vers le récepteur de notifications à encapsuler.</span><span class="sxs-lookup"><span data-stu-id="af6ea-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="af6ea-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="af6ea-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="af6ea-116">[out] Pointeur vers un pointeur vers un nouveau récepteur de notifications qui encapsule le récepteur de notifications indiqué par le paramètre _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="af6ea-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="af6ea-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af6ea-117">Return value</span></span>

<span data-ttu-id="af6ea-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="af6ea-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af6ea-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="af6ea-119">Remarks</span></span>

<span data-ttu-id="af6ea-120">L’objectif du wrapper est pour vous assurer que la notification est appelée sur le même thread qui a appelé la fonction **HrThisThreadAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="af6ea-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="af6ea-121">Cette fonction est utilisée pour protéger les rappels de notification qui doivent s’exécuter sur un thread particulier.</span><span class="sxs-lookup"><span data-stu-id="af6ea-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="af6ea-122">Applications clientes permet de limiter les notifications sont générées, autrement dit, lors des appels à la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de l’objet de récepteur advise transmis par le client dans une précédente **Advise **HrThisThreadAdviseSink** **d’appel.</span><span class="sxs-lookup"><span data-stu-id="af6ea-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="af6ea-123">Si les notifications sont autorisées à générer arbitrairement, une implémentation de notification peut forcer un client dans opération multithread lorsque qui ne serait pas appropriée.</span><span class="sxs-lookup"><span data-stu-id="af6ea-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="af6ea-124">Par exemple, un client peut utiliser une bibliothèque, telle qu’une des bibliothèques de classes Microsoft Foundation, qui ne prend pas en charge les appels multithreads.</span><span class="sxs-lookup"><span data-stu-id="af6ea-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="af6ea-125">Notification sur un autre thread qu’un tel client difficile à tester et source d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="af6ea-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="af6ea-126">**HrThisThreadAdviseSink** permet de s’assurer que les appels **OnNotify** se produisent uniquement à ces heures appropriés :</span><span class="sxs-lookup"><span data-stu-id="af6ea-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="af6ea-127">Lors du traitement d’un appel à n’importe quelle méthode MAPI.</span><span class="sxs-lookup"><span data-stu-id="af6ea-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="af6ea-128">Lors du traitement des messages Windows.</span><span class="sxs-lookup"><span data-stu-id="af6ea-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="af6ea-129">Lorsque **HrThisThreadAdviseSink** est implémentée, les appels à **OnNotify** (méthode) du nouveau récepteur advise sur n’importe quel thread entraînent la méthode de notification d’origine à exécuter sur le thread sur lequel **HrThisThreadAdviseSink** a été appelée.</span><span class="sxs-lookup"><span data-stu-id="af6ea-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="af6ea-130">Pour plus d’informations sur la notification et les récepteurs de notifications, voir [Notification d’événement MAPI](event-notification-in-mapi.md) et [l’implémentation d’un objet récepteur de notification](implementing-an-advise-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="af6ea-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

