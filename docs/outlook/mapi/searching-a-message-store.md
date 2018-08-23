---
title: Recherche dans une banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 74b63719f6d72e3c92cbcef6fdb26ee106d4b9aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571835"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="22dfc-103">Recherche dans une banque de messages</span><span class="sxs-lookup"><span data-stu-id="22dfc-103">Searching a message store</span></span>

<span data-ttu-id="22dfc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22dfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22dfc-105">Applications clientes peuvent parcourir un ou plusieurs dossiers de rechercher les messages qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="22dfc-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="22dfc-106">La technique la plus simple de recherche implique l’application d’une restriction pour définir les critères et placer les résultats dans un dossier de résultats de recherche, créé explicitement de la recherche ou une recherche précédente.</span><span class="sxs-lookup"><span data-stu-id="22dfc-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="22dfc-107">Pas de toutes les banques de messages prennent en charge cette technique.</span><span class="sxs-lookup"><span data-stu-id="22dfc-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="22dfc-108">Pour déterminer si la banque de messages que vous utilisez prend en charge l’utilisation de dossiers de résultats de recherche, appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer la **PR\_STORE_SUPPORT_MASK** propriété ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="22dfc-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="22dfc-109">Si l’indicateur STORE_SEARCH_OK est défini, la recherche est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="22dfc-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="22dfc-110">Si elle n’est pas définie, vous aurez besoin d’une autre approche telles que l’inspection manuellement les dossiers cible.</span><span class="sxs-lookup"><span data-stu-id="22dfc-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="22dfc-111">Pour rechercher un ou plusieurs dossiers dans une banque de messages</span><span class="sxs-lookup"><span data-stu-id="22dfc-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="22dfc-112">Si vous disposez d’un dossier de résultats de recherche à partir d’une recherche précédente, passez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="22dfc-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="22dfc-113">Dans le cas contraire, pour créer un dossier de résultats de recherche :</span><span class="sxs-lookup"><span data-stu-id="22dfc-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="22dfc-114">Récupérer l’identificateur d’entrée pour le dossier racine de résultats de recherche à l’appel de méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages et demande **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="22dfc-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="22dfc-115">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir le dossier représenté par PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="22dfc-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="22dfc-116">Appeler la méthode de [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) du dossier pour créer un dossier de résultats de recherche avec l’indicateur FOLDER_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="22dfc-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="22dfc-117">Créer une restriction pour stocker vos critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="22dfc-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="22dfc-118">Créer un tableau d’identificateurs d’entrée qui représentent les dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="22dfc-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="22dfc-119">Cette étape est inutile si le dossier de résultats de recherche n’a été utilisé et que vous souhaitez les mêmes dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="22dfc-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="22dfc-120">Appelez méthode pointant _lpContainerList_ sur le tableau d’identificateur de l’entrée et _lpRestriction_ à la restriction [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="22dfc-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="22dfc-121">Si vous avez enregistré les notifications complète de recherche avec la banque de messages, attendez que la notification d’arriver.</span><span class="sxs-lookup"><span data-stu-id="22dfc-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="22dfc-122">Afficher les résultats de la recherche par la méthode les résultats de recherche du dossier [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pour accéder à sa table de contenu.</span><span class="sxs-lookup"><span data-stu-id="22dfc-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="22dfc-123">Appelez le contenu [IMAPITable::QueryRows](imapitable-queryrows.md) méthode table pour récupérer les messages qui satisfont les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="22dfc-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

