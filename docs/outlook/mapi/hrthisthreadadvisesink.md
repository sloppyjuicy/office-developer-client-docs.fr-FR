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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427726"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="c956c-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c956c-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="c956c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c956c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c956c-105">Crée un sink de conseil qui encapsule un sink de conseil existant pour la sécurité des threads.</span><span class="sxs-lookup"><span data-stu-id="c956c-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c956c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c956c-106">Header file:</span></span>  <br/> |<span data-ttu-id="c956c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c956c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c956c-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c956c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c956c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c956c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c956c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c956c-110">Called by:</span></span>  <br/> |<span data-ttu-id="c956c-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="c956c-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="c956c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="c956c-112">Parameters</span></span>

 <span data-ttu-id="c956c-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c956c-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c956c-114">[in] Pointeur vers le sink de conseil à wrapped.</span><span class="sxs-lookup"><span data-stu-id="c956c-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="c956c-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c956c-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="c956c-116">[out] Pointeur vers un pointeur vers un nouveau sink de conseil qui encapsule le sink advise pointé par _le paramètre lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="c956c-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c956c-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c956c-117">Return value</span></span>

<span data-ttu-id="c956c-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c956c-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c956c-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="c956c-119">Remarks</span></span>

<span data-ttu-id="c956c-120">L’objectif du wrapper est de s’assurer que la notification est appelée sur le même thread que celui qui a appelé la fonction **HrThisThreadAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="c956c-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="c956c-121">Cette fonction est utilisée pour protéger les rappels de notification qui doivent s’exécuter sur un thread particulier.</span><span class="sxs-lookup"><span data-stu-id="c956c-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="c956c-122">Les applications clientes doivent utiliser **HrThisThreadAdviseSink** pour limiter le moment où des notifications sont générées, c’est-à-dire lorsque des appels sont  effectués à la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de l’objet de réception de notification transmis par le client dans un appel de conseil précédent.</span><span class="sxs-lookup"><span data-stu-id="c956c-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="c956c-123">Si les notifications sont autorisées à être générées arbitrairement, une implémentation de notification peut forcer un client à une opération multithread alors que cela ne serait pas approprié.</span><span class="sxs-lookup"><span data-stu-id="c956c-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="c956c-124">Par exemple, un client peut utiliser une bibliothèque, telle que l’une des bibliothèques de classes Microsoft Foundation, qui ne prend pas en charge les appels multithread.</span><span class="sxs-lookup"><span data-stu-id="c956c-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="c956c-125">Une notification sur un autre thread rendrait un tel client difficile à tester et sujette à des erreurs.</span><span class="sxs-lookup"><span data-stu-id="c956c-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="c956c-126">**HrThisThreadAdviseSink** s’assure que les appels **OnNotify** se produisent uniquement aux moments appropriés :</span><span class="sxs-lookup"><span data-stu-id="c956c-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="c956c-127">Pendant le traitement d’un appel à n’importe quelle méthode MAPI.</span><span class="sxs-lookup"><span data-stu-id="c956c-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="c956c-128">Pendant le traitement des Windows messages.</span><span class="sxs-lookup"><span data-stu-id="c956c-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="c956c-129">Lorsque **HrThisThreadAdviseSink** est implémenté, tous les appels à la méthode **OnNotify** du nouveau sink de notification sur n’importe quel thread entraînent l’exécution de la méthode de notification d’origine sur le thread sur lequel **HrThisThreadAdviseSink** a été appelé.</span><span class="sxs-lookup"><span data-stu-id="c956c-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="c956c-130">Pour plus d’informations sur les réceptions de notification et de notification, consultez la notification d’événement dans [MAPI](event-notification-in-mapi.md) et [l’implémentation d’un objet de réception de notification.](implementing-an-advise-sink-object.md)</span><span class="sxs-lookup"><span data-stu-id="c956c-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

