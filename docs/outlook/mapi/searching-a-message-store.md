---
title: Recherche dans une banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 90ed7da43d7f9e5e8b5f3024f1eee99a2d7a2b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787094"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="a6f6c-103">Recherche dans une banque de messages</span><span class="sxs-lookup"><span data-stu-id="a6f6c-103">Searching a message store</span></span>

<span data-ttu-id="a6f6c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6f6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6f6c-105">Applications clientes peuvent parcourir un ou plusieurs dossiers de rechercher les messages qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="a6f6c-106">La technique la plus simple de recherche implique l’application d’une restriction pour définir les critères et placer les résultats dans un dossier de résultats de recherche, créé explicitement de la recherche ou une recherche précédente.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="a6f6c-107">Pas de toutes les banques de messages prennent en charge cette technique.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="a6f6c-108">Pour déterminer si la banque de messages que vous utilisez prend en charge l’utilisation de dossiers de résultats de recherche, appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer la **PR\_STORE_SUPPORT_MASK** propriété ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a6f6c-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="a6f6c-109">Si l’indicateur STORE_SEARCH_OK est défini, la recherche est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="a6f6c-110">Si elle n’est pas définie, vous aurez besoin d’une autre approche telles que l’inspection manuellement les dossiers cible.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="a6f6c-111">Pour rechercher un ou plusieurs dossiers dans une banque de messages</span><span class="sxs-lookup"><span data-stu-id="a6f6c-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="a6f6c-112">Si vous disposez d’un dossier de résultats de recherche à partir d’une recherche précédente, passez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="a6f6c-113">Dans le cas contraire, pour créer un dossier de résultats de recherche :</span><span class="sxs-lookup"><span data-stu-id="a6f6c-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="a6f6c-114">Récupérer l’identificateur d’entrée pour le dossier racine de résultats de recherche à l’appel de méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages et demande **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a6f6c-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="a6f6c-115">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir le dossier représenté par PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="a6f6c-116">Appeler la méthode de [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) du dossier pour créer un dossier de résultats de recherche avec l’indicateur FOLDER_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="a6f6c-117">Créer une restriction pour stocker vos critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="a6f6c-118">Créer un tableau d’identificateurs d’entrée qui représentent les dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="a6f6c-119">Cette étape est inutile si le dossier de résultats de recherche n’a été utilisé et que vous souhaitez les mêmes dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="a6f6c-120">Appelez méthode pointant _lpContainerList_ sur le tableau d’identificateur de l’entrée et _lpRestriction_ à la restriction [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="a6f6c-121">Si vous avez enregistré les notifications complète de recherche avec la banque de messages, attendez que la notification d’arriver.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="a6f6c-122">Afficher les résultats de la recherche par la méthode les résultats de recherche du dossier [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pour accéder à sa table de contenu.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="a6f6c-123">Appelez le contenu [IMAPITable::QueryRows](imapitable-queryrows.md) méthode table pour récupérer les messages qui satisfont les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="a6f6c-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

