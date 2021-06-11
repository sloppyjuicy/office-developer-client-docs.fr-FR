---
title: À propos Notification-Based'indexation du Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409173"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="89435-103">À propos Notification-Based'indexation du Store</span><span class="sxs-lookup"><span data-stu-id="89435-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="89435-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89435-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89435-105">Un fournisseur de magasin MAPI peut spécifier si le fournisseur de protocole MAPI analyse et indexe les messages dans la boutique, ou si la boutique envoie des notifications à l’indexeur lorsqu’il existe des messages à indexer.</span><span class="sxs-lookup"><span data-stu-id="89435-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="89435-106">Ce dernier est connu sous le nom d’indexation basée sur les notifications et un magasin qui prend en charge l’indexation basée sur les notifications est un magasin de push.</span><span class="sxs-lookup"><span data-stu-id="89435-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="89435-107">Un fournisseur de magasins qui prend en charge l’indexation basée sur les notifications définit **l’STORE_PUSHER_OK** dans la **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** de données.</span><span class="sxs-lookup"><span data-stu-id="89435-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="89435-108">Le handler de protocole MAPI ou un client peut obtenir la propriété **PR_STORE_SUPPORT_MASK** pour déterminer les caractéristiques du magasin.</span><span class="sxs-lookup"><span data-stu-id="89435-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="89435-109">Chaque fois qu’une pièce jointe, un dossier ou un message doit être indexé, le fournisseur de magasins génère une URL (Uniform Resource Locator) MAPI identifiant l’objet à indexer et l’envoie à l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="89435-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="89435-110">Cette URL MAPI est codée en Unicode et doit identifier de manière unique l’objet dans le handler de protocole MAPI.</span><span class="sxs-lookup"><span data-stu-id="89435-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="89435-111">Pour plus d’informations sur les URL MAPI, voir À propos des URL MAPI pour [lNotification-Based indexation.](about-mapi-urls-for-notification-based-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="89435-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="89435-112">Étant donné qu’un indexeur ne peut pas toujours indexer tous les détails avant qu’un arrêt ne se produise dans un magasin de pusher, celui-ci doit conserver ce qui doit être poussée.</span><span class="sxs-lookup"><span data-stu-id="89435-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="89435-113">Lorsqu’un fournisseur de magasin envoie une notification sur un objet qui doit être indexé, il spécifie le type de notification **fnevIndexing** dans le membre **ulEventType** de la structure **[NOTIFICATION.](notification.md)**</span><span class="sxs-lookup"><span data-stu-id="89435-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="89435-114">Le membre **info** de la structure **NOTIFICATION** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)**.</span><span class="sxs-lookup"><span data-stu-id="89435-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="89435-115">Le fournisseur de magasin identifie le processus dans la **[propriété PR_SEARCH_OWNER_ID.](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="89435-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="89435-116">Il identifie également le processus dans la structure [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) et transmet ces informations dans le cadre du membre **pbEventParameters** de la structure **EXTENDED_NOTIFICATION.**</span><span class="sxs-lookup"><span data-stu-id="89435-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="89435-117">Si le processus est arrêté ou se ferme, le handler de protocole MAPI sera en mesure de détecter cela immédiatement et d’arrêter l’indexation du magasin de pusher.</span><span class="sxs-lookup"><span data-stu-id="89435-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89435-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89435-118">See also</span></span>



[<span data-ttu-id="89435-119">À propos de l’API de magasin</span><span class="sxs-lookup"><span data-stu-id="89435-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="89435-120">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="89435-120">MAPI Constants</span></span>](mapi-constants.md)

