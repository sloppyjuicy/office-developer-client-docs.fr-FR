---
title: À propos de l’API du magasin
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 31aff61ec5868b0f1e9ab34d498b2e8175519f0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782877"
---
# <a name="about-the-store-api"></a><span data-ttu-id="c0180-103">À propos de l’API du magasin</span><span class="sxs-lookup"><span data-stu-id="c0180-103">About the Store API</span></span>

  
  
<span data-ttu-id="c0180-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0180-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0180-105">L’API stocker fournit la fonctionnalité de magasin de divers pour stocker les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="c0180-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="c0180-106">Il fournit les définitions, types de données, propriétés et interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0180-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="c0180-107">Définitions :</span><span class="sxs-lookup"><span data-stu-id="c0180-107">Definitions:</span></span>
  
- [<span data-ttu-id="c0180-108">Constantes pour l’API du magasin</span><span class="sxs-lookup"><span data-stu-id="c0180-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="c0180-109">Types de données :</span><span class="sxs-lookup"><span data-stu-id="c0180-109">Data types:</span></span>
  
- <span data-ttu-id="c0180-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="c0180-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="c0180-112">Propriétés nommées :</span><span class="sxs-lookup"><span data-stu-id="c0180-112">Named Properties:</span></span>
  
- <span data-ttu-id="c0180-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="c0180-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="c0180-115">**[Afficher les tailles de dossier de serveur](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="c0180-116">**[Masquer l’Option de mise à jour de réunion](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="c0180-117">**[Magasin de marque Type privé](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="c0180-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="c0180-119">Fournisseurs de magasins qui ne nécessitent pas une des fonctionnalités offertes par ces propriétés nommées peuvent simplement les ignorer et implémenter pas prise en charge dans l’interface **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="c0180-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="c0180-120">Étant donné que ces propriétés sont fournies à partir de Microsoft Outlook 2003 Service Pack 1, en les ajoutant à un magasin dans une version antérieure de Microsoft Outlook n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="c0180-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="c0180-121">Ils sont ignorés s’ils n’existent pas ou si sa valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="c0180-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="c0180-122">Propriétés :</span><span class="sxs-lookup"><span data-stu-id="c0180-122">Properties:</span></span>
  
- <span data-ttu-id="c0180-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="c0180-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="c0180-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="c0180-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="c0180-127">Interfaces :</span><span class="sxs-lookup"><span data-stu-id="c0180-127">Interfaces:</span></span>
  
- <span data-ttu-id="c0180-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="c0180-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="c0180-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="c0180-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="c0180-131">Inscription des magasins pour l’indexation</span><span class="sxs-lookup"><span data-stu-id="c0180-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="c0180-132">Le Gestionnaire de protocole MAPI vérifie le Registre Windows pour les magasins il doit indexer à des fins de recherche.</span><span class="sxs-lookup"><span data-stu-id="c0180-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="c0180-133">Fournisseurs de magasins indexer doivent être enregistrés dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="c0180-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="c0180-134">Pour plus d’informations sur l’inscription des fournisseurs de magasins pour l’indexation dans Outlook 2013 ou Outlook 2010, voir [Sur inscription magasins pour l’indexation](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="c0180-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="c0180-135">L’indexation des magasins</span><span class="sxs-lookup"><span data-stu-id="c0180-135">Indexing Stores</span></span>

<span data-ttu-id="c0180-136">Fournisseurs de magasins MAPI peuvent choisir d’autoriser le Gestionnaire de protocole MAPI pour analyser et indexer les messages dans le magasin, ou envoyer des notifications à l’indexeur que s’il existe des messages à indexer.</span><span class="sxs-lookup"><span data-stu-id="c0180-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="c0180-137">Pour plus d’informations sur l’indexation basée sur les notifications, voir [L’indexation du magasin About Notification-Based](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="c0180-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

