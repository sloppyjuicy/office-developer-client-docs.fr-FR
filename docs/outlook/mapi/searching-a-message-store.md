---
title: Recherche d’un message dans une banque
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
ms.openlocfilehash: 13b54d4220bb2f0b89959e9188093ecc36d981ea
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376083"
---
# <a name="searching-a-message-store"></a>Recherche d’un message dans une banque

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes peuvent rechercher dans un ou plusieurs dossiers la recherche de messages qui correspondent aux critères de recherche. La technique de recherche la plus simple consiste à appliquer une restriction pour définir des critères et à placer les résultats dans un dossier de résultats de recherche, créé explicitement pour cette recherche ou pour une recherche antérieure. Toutes les magasins de messages ne la prisent pas en charge. 

Pour déterminer si la boutique de messages que vous utilisez prend en charge l’utilisation des dossiers de résultats de recherche, appelez sa méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer la propriété **PR\_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si l’STORE_SEARCH_OK est définie, la recherche est prise en charge. Si elle n’est pas définie, vous aurez besoin d’une autre approche, telle que l’inspection manuelle des dossiers cibles.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Pour rechercher un ou plusieurs dossiers dans une magasin de messages
  
1. Si vous avez un dossier de résultats de recherche d’une recherche précédente, passez à l’étape 2. Dans le cas contraire, pour créer un dossier de résultats de recherche :
    
    1. Récupérez l’identificateur d’entrée pour le dossier racine des résultats de la recherche en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la boutique de messages et en demandant **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).
        
    2. [Appelez IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir le dossier représenté par PR_FINDER_ENTRYID. 
        
    3. Appelez la méthode [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) du dossier pour créer un dossier de résultats de recherche avec l’indicateur FOLDER_SEARCH de recherche. 
    
2. Créez une restriction pour contenir vos critères de recherche. 
    
3. Créez un tableau d’identificateurs d’entrée qui représentent les dossiers à rechercher. Cette étape est inutile si le dossier de résultats de recherche a déjà été utilisé et que vous souhaitez effectuer une recherche dans les mêmes dossiers.
    
4. Appelez la méthode [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier de résultats de recherche, en pointant  _lpContainerList_ vers le tableau d’identificateurs d’entrée et  _lpRestriction_ vers la restriction. 
    
5. Si vous vous êtes inscrit aux notifications de fin de recherche auprès de la boutique de messages, attendez que la notification arrive.
    
6. Affichez les résultats de la recherche en appelant la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) du dossier de résultats de recherche pour accéder à sa table des matières. 
    
7. Appelez la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) de la table des matières pour récupérer les messages qui répondent aux critères de recherche. 
    

