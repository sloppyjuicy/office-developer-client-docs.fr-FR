---
title: À propos de l’API de magasin
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405554"
---
# <a name="about-the-store-api"></a><span data-ttu-id="c19d7-103">À propos de l’API de magasin</span><span class="sxs-lookup"><span data-stu-id="c19d7-103">About the Store API</span></span>

  
  
<span data-ttu-id="c19d7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c19d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c19d7-105">L’API Store fournit diverses fonctionnalités du Store aux fournisseurs de magasins.</span><span class="sxs-lookup"><span data-stu-id="c19d7-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="c19d7-106">Il fournit les définitions, types de données, propriétés et interfaces suivants.</span><span class="sxs-lookup"><span data-stu-id="c19d7-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="c19d7-107">Définitions :</span><span class="sxs-lookup"><span data-stu-id="c19d7-107">Definitions:</span></span>
  
- [<span data-ttu-id="c19d7-108">Constantes de l’API du Store</span><span class="sxs-lookup"><span data-stu-id="c19d7-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="c19d7-109">Types de données :</span><span class="sxs-lookup"><span data-stu-id="c19d7-109">Data types:</span></span>
  
- <span data-ttu-id="c19d7-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="c19d7-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="c19d7-112">Propriétés nommées :</span><span class="sxs-lookup"><span data-stu-id="c19d7-112">Named Properties:</span></span>
  
- <span data-ttu-id="c19d7-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="c19d7-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="c19d7-115">**[Tailles des dossiers du serveur d’affichage](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="c19d7-116">**[Masquer l’option de mise à jour de réunion](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="c19d7-117">**[Rendre privé le type de magasin](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="c19d7-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="c19d7-119">Les fournisseurs de magasins qui ne nécessitent aucune des fonctionnalités offertes par ces propriétés nommées peuvent simplement les ignorer et ne pas implémenter la prise en charge dans l’interface **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="c19d7-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="c19d7-120">Étant donné que ces propriétés sont fournies à partir de Microsoft Outlook 2003 Service Pack 1, leur ajout à un magasin dans une version antérieure de Microsoft Outlook n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="c19d7-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="c19d7-121">Ils sont ignorés s’ils n’existent pas ou si leur valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="c19d7-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="c19d7-122">Propriétés :</span><span class="sxs-lookup"><span data-stu-id="c19d7-122">Properties:</span></span>
  
- <span data-ttu-id="c19d7-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="c19d7-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="c19d7-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="c19d7-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="c19d7-127">Interfaces :</span><span class="sxs-lookup"><span data-stu-id="c19d7-127">Interfaces:</span></span>
  
- <span data-ttu-id="c19d7-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="c19d7-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="c19d7-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="c19d7-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="c19d7-131">Inscription de magasins pour l’indexation</span><span class="sxs-lookup"><span data-stu-id="c19d7-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="c19d7-132">Le handler de protocole MAPI vérifie dans le Registre Windows les magasins qu’il doit indexer à des fins de recherche.</span><span class="sxs-lookup"><span data-stu-id="c19d7-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="c19d7-133">Les fournisseurs du Windows Store qui souhaitent être indexés doivent être inscrits dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="c19d7-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="c19d7-134">Pour plus d’informations sur l’inscription de fournisseurs de magasins pour l’indexation dans Outlook 2013 ou Outlook 2010, voir à propos de l’inscription des magasins pour [l’indexation.](about-registering-stores-for-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="c19d7-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="c19d7-135">Magasins d’indexation</span><span class="sxs-lookup"><span data-stu-id="c19d7-135">Indexing Stores</span></span>

<span data-ttu-id="c19d7-136">Les fournisseurs de magasins MAPI peuvent choisir d’autoriser le handler de protocole MAPI à analyser et indexer des messages dans la boutique, ou d’envoyer des notifications à l’indexeur uniquement lorsqu’il existe des messages à indexer.</span><span class="sxs-lookup"><span data-stu-id="c19d7-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="c19d7-137">Pour plus d’informations sur l’indexation basée sur les notifications, voir à propos [Notification-Based'indexation dans le Store.](about-notification-based-store-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="c19d7-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

