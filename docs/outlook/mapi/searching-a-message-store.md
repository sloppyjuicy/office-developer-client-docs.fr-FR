---
title: Recherche d’un message dans une banque
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426036"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="13ecf-103">Recherche d’un message dans une banque</span><span class="sxs-lookup"><span data-stu-id="13ecf-103">Searching a message store</span></span>

<span data-ttu-id="13ecf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13ecf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13ecf-105">Les applications clientes peuvent rechercher dans un ou plusieurs dossiers la recherche de messages qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="13ecf-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="13ecf-106">La technique de recherche la plus simple consiste à appliquer une restriction pour définir des critères et à placer les résultats dans un dossier de résultats de recherche, créé explicitement pour cette recherche ou pour une recherche antérieure.</span><span class="sxs-lookup"><span data-stu-id="13ecf-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="13ecf-107">Toutes les magasins de messages ne la prisent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="13ecf-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="13ecf-108">Pour déterminer si la boutique de messages que vous utilisez prend en charge l’utilisation des dossiers de résultats de recherche, appelez sa méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer la propriété **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="13ecf-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="13ecf-109">Si l’STORE_SEARCH_OK est définie, la recherche est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13ecf-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="13ecf-110">Si elle n’est pas définie, vous aurez besoin d’une autre approche, telle que l’inspection manuelle des dossiers cibles.</span><span class="sxs-lookup"><span data-stu-id="13ecf-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="13ecf-111">Pour rechercher un ou plusieurs dossiers dans une magasin de messages</span><span class="sxs-lookup"><span data-stu-id="13ecf-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="13ecf-112">Si vous avez un dossier de résultats de recherche d’une recherche précédente, passez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="13ecf-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="13ecf-113">Dans le cas contraire, pour créer un dossier de résultats de recherche :</span><span class="sxs-lookup"><span data-stu-id="13ecf-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="13ecf-114">Récupérez l’identificateur d’entrée pour le dossier racine des résultats de la recherche en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la boutique de messages et en demandant **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="13ecf-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="13ecf-115">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir le dossier représenté par PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="13ecf-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="13ecf-116">Appelez la méthode [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) du dossier pour créer un dossier de résultats de recherche avec l’indicateur FOLDER_SEARCH de recherche.</span><span class="sxs-lookup"><span data-stu-id="13ecf-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="13ecf-117">Créez une restriction pour contenir vos critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="13ecf-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="13ecf-118">Créez un tableau d’identificateurs d’entrée qui représentent les dossiers à rechercher.</span><span class="sxs-lookup"><span data-stu-id="13ecf-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="13ecf-119">Cette étape est inutile si le dossier de résultats de recherche a déjà été utilisé et que vous souhaitez effectuer une recherche dans les mêmes dossiers.</span><span class="sxs-lookup"><span data-stu-id="13ecf-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="13ecf-120">Appelez la méthode [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier de résultats de recherche, en pointant  _lpContainerList_ vers le tableau d’identificateurs d’entrée et  _lpRestriction_ vers la restriction.</span><span class="sxs-lookup"><span data-stu-id="13ecf-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="13ecf-121">Si vous vous êtes inscrit aux notifications de fin de recherche auprès de la boutique de messages, attendez que la notification arrive.</span><span class="sxs-lookup"><span data-stu-id="13ecf-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="13ecf-122">Affichez les résultats de la recherche en appelant la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) du dossier de résultats de recherche pour accéder à sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="13ecf-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="13ecf-123">Appelez la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) de la table des matières pour récupérer les messages qui répondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="13ecf-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

