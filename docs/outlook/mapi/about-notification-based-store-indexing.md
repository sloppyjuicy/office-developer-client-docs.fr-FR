---
title: À propos de l'indexation du magasin basé sur les notifications
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322133"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="319ab-103">À propos de l'indexation du magasin basé sur les notifications</span><span class="sxs-lookup"><span data-stu-id="319ab-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="319ab-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="319ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="319ab-105">Un fournisseur de banque MAPI peut spécifier si le gestionnaire de protocole MAPI analyse et indexe les messages dans la Banque, ou si le magasin envoie des notifications à l'indexeur lorsque des messages sont indexés.</span><span class="sxs-lookup"><span data-stu-id="319ab-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="319ab-106">Ce dernier est appelé indexation basée sur les notifications, et un magasin qui prend en charge l'indexation basée sur les notifications est appelé magasin de diffuseurs.</span><span class="sxs-lookup"><span data-stu-id="319ab-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="319ab-107">Un fournisseur de banque qui prend en charge l'indexation basée sur la notification définit l'indicateur **STORE_PUSHER_OK** dans la propriété **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="319ab-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="319ab-108">Le gestionnaire de protocole MAPI ou un client peut obtenir la propriété **PR_STORE_SUPPORT_MASK** pour déterminer les caractéristiques de la Banque.</span><span class="sxs-lookup"><span data-stu-id="319ab-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="319ab-109">Chaque fois qu'une pièce jointe, un dossier ou un message doit être indexé, le fournisseur de banque d'adresses génère une URL (Uniform Resource Locator) MAPI qui identifie l'objet à indexer et l'envoie à l'indexeur.</span><span class="sxs-lookup"><span data-stu-id="319ab-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="319ab-110">Cette URL MAPI est codée en Unicode et doit identifier de manière unique l'objet dans le gestionnaire de protocole MAPI.</span><span class="sxs-lookup"><span data-stu-id="319ab-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="319ab-111">Pour plus d'informations sur les URL MAPI, reportez-vous à la rubrique [à propos des URL MAPI pour l'indexation basée sur les notifications](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="319ab-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="319ab-112">Étant donné qu'un indexeur ne peut pas toujours indexer tous les éléments avant qu'un arrêt ait lieu dans un magasin de pousseurs, le magasin de Push doit conserver ce qui doit être poussé.</span><span class="sxs-lookup"><span data-stu-id="319ab-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="319ab-113">Lorsqu'un fournisseur de banque d'informations envoie une notification sur un objet qui doit être indexé, il spécifie le type de notification **fnevIndexing** dans le membre **ulEventType** de la structure de **[notification](notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="319ab-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="319ab-114">Le membre **info** de la structure **NOTIFICATION** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)**.</span><span class="sxs-lookup"><span data-stu-id="319ab-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="319ab-115">Le fournisseur Store identifie le processus dans la propriété **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="319ab-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="319ab-116">Il identifie également le processus dans la structure [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) et transmet ces informations dans le cadre du membre **pbEventParameters** de la structure **EXTENDED_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="319ab-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="319ab-117">Si le processus est arrêté ou se bloque, le gestionnaire de protocole MAPI pourra immédiatement le détecter et arrêter l'indexation du magasin de transmission de contenu.</span><span class="sxs-lookup"><span data-stu-id="319ab-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="319ab-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="319ab-118">See also</span></span>



[<span data-ttu-id="319ab-119">À propos de l’API de magasin</span><span class="sxs-lookup"><span data-stu-id="319ab-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="319ab-120">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="319ab-120">MAPI Constants</span></span>](mapi-constants.md)

