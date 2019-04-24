---
title: Recherche d’un message dans une banque
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338800"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="abfbd-103">Recherche d’un message dans une banque</span><span class="sxs-lookup"><span data-stu-id="abfbd-103">Searching a message store</span></span>

<span data-ttu-id="abfbd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abfbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abfbd-105">Les applications clientes peuvent effectuer des recherches dans un ou plusieurs dossiers à la recherche de messages qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="abfbd-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="abfbd-106">La technique de recherche la plus simple consiste à appliquer une restriction pour définir des critères et à placer les résultats dans un dossier de résultats de recherche, créé explicitement pour cette recherche ou pour une recherche préalable.</span><span class="sxs-lookup"><span data-stu-id="abfbd-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="abfbd-107">Toutes les banques de messages ne prennent pas en charge cette technique.</span><span class="sxs-lookup"><span data-stu-id="abfbd-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="abfbd-108">Pour déterminer si la Banque de messages que vous utilisez prend en charge à l'aide des dossiers de résultats de recherche, appelez sa méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) pour récupérer la propriété **\_PR STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="abfbd-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="abfbd-109">Si l'indicateur STORE_SEARCH_OK est défini, la recherche est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="abfbd-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="abfbd-110">Si ce n'est pas le cas, vous aurez besoin d'une autre approche, telle que l'inspection manuelle des dossiers cibles.</span><span class="sxs-lookup"><span data-stu-id="abfbd-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="abfbd-111">Pour rechercher un ou plusieurs dossiers dans une banque de messages</span><span class="sxs-lookup"><span data-stu-id="abfbd-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="abfbd-112">Si vous disposez d'un dossier Search-Results d'une recherche précédente, passez à l'étape 2.</span><span class="sxs-lookup"><span data-stu-id="abfbd-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="abfbd-113">Dans le cas contraire, pour créer un dossier de résultats de recherche, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="abfbd-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="abfbd-114">Récupérez l'identificateur d'entrée pour le dossier racine de résultats de recherche en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages et en demandant **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="abfbd-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="abfbd-115">Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) pour ouvrir le dossier représenté par PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="abfbd-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="abfbd-116">Appelez la méthode [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) pour créer un dossier de résultats de recherche avec l'indicateur FOLDER_SEARCH défini.</span><span class="sxs-lookup"><span data-stu-id="abfbd-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="abfbd-117">Créez une restriction pour conserver vos critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="abfbd-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="abfbd-118">Créez un tableau d'identificateurs d'entrée qui représentent les dossiers à rechercher.</span><span class="sxs-lookup"><span data-stu-id="abfbd-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="abfbd-119">Cette étape n'est pas nécessaire si le dossier Search-Results a été utilisé avant et que vous souhaitez effectuer des recherches dans les mêmes dossiers.</span><span class="sxs-lookup"><span data-stu-id="abfbd-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="abfbd-120">Appelez la méthode [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier Search-Results, puis pointez _lpContainerList_ vers le tableau de l'identificateur d'entrée et _lpRestriction_ à la restriction.</span><span class="sxs-lookup"><span data-stu-id="abfbd-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="abfbd-121">Si vous vous êtes inscrit pour les notifications d'exécution de la recherche avec la Banque de messages, patientez jusqu'à ce que la notification arrive.</span><span class="sxs-lookup"><span data-stu-id="abfbd-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="abfbd-122">Affichez les résultats de la recherche en appelant la méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) du dossier Search-Results pour accéder à sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="abfbd-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="abfbd-123">Appelez la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire les messages qui satisfont les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="abfbd-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

