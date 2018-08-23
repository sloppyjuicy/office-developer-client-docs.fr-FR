---
title: À propos de l’indexation de magasin basée sur une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 125147ed7d6cd90c1069aa5cc1c759abe752dfe2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564520"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="fb63e-103">À propos de l’indexation de magasin basée sur une notification</span><span class="sxs-lookup"><span data-stu-id="fb63e-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="fb63e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb63e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb63e-105">Un fournisseur de banque MAPI peut spécifier si les analyses de gestionnaire de protocole MAPI et les index des messages dans le magasin, ou si la banque envoie des notifications à l’indexeur lorsqu’il existe des messages à indexer.</span><span class="sxs-lookup"><span data-stu-id="fb63e-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="fb63e-106">Ce dernier est connu en tant que l’indexation basée sur une notification, et un objet store qui prend en charge l’indexation basée sur une notification est connu comme un magasin poussoir.</span><span class="sxs-lookup"><span data-stu-id="fb63e-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="fb63e-107">Un fournisseur de banque prend en charge les jeux d’indexation de notification l’indicateur **STORE_PUSHER_OK** dans la propriété **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="fb63e-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="fb63e-108">Le Gestionnaire de protocole MAPI ou d’un client peut obtenir la propriété **PR_STORE_SUPPORT_MASK** pour déterminer les caractéristiques de la banque.</span><span class="sxs-lookup"><span data-stu-id="fb63e-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="fb63e-109">Chaque fois qu’il existe une pièce jointe, dossier ou un message à indexer, le fournisseur de banque génère un MAPI URL Uniform Resource Locator () qui identifie l’objet à indexer et l’envoie à l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="fb63e-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="fb63e-110">Cette URL MAPI est codée en Unicode et doit identifier de manière unique l’objet dans le Gestionnaire de protocole MAPI.</span><span class="sxs-lookup"><span data-stu-id="fb63e-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="fb63e-111">Pour plus d’informations sur les URL MAPI, voir [Sur les URL MAPI pour l’indexation basée sur une Notification](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="fb63e-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="fb63e-112">Un indexeur ne peut pas toujours indexer tout avant un arrêt se produit dans une banque poussoir, la banque poussoir doit conserve les éléments qui doivent être appliquées.</span><span class="sxs-lookup"><span data-stu-id="fb63e-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="fb63e-113">Lorsqu’un fournisseur de banque envoie une notification relative à un objet qui doit être indexé, elle spécifie le type de notification **fnevIndexing** dans le membre **ulEventType** de la structure de **[NOTIFICATION](notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="fb63e-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="fb63e-114">Membre de la structure de **NOTIFICATION** **info** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="fb63e-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="fb63e-115">Le fournisseur de banque identifie le processus dans la propriété **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="fb63e-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="fb63e-116">Il identifie le processus de la structure [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) et vous transmet ces informations dans le cadre du membre de la structure **EXTENDED_NOTIFICATION** **pbEventParameters** .</span><span class="sxs-lookup"><span data-stu-id="fb63e-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="fb63e-117">Si le processus est arrêté ou se bloque, le Gestionnaire de protocole MAPI sera en mesure de détecter et arrêter l’indexation de la banque poussoir immédiatement.</span><span class="sxs-lookup"><span data-stu-id="fb63e-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb63e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb63e-118">See also</span></span>



[<span data-ttu-id="fb63e-119">À propos de l’API de magasin</span><span class="sxs-lookup"><span data-stu-id="fb63e-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="fb63e-120">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fb63e-120">MAPI Constants</span></span>](mapi-constants.md)

