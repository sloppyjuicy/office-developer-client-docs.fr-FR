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
# <a name="searching-a-message-store"></a>Recherche dans une banque de messages

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Applications clientes peuvent parcourir un ou plusieurs dossiers de rechercher les messages qui correspondent aux critères de recherche. La technique la plus simple de recherche implique l’application d’une restriction pour définir les critères et placer les résultats dans un dossier de résultats de recherche, créé explicitement de la recherche ou une recherche précédente. Pas de toutes les banques de messages prennent en charge cette technique. 

Pour déterminer si la banque de messages que vous utilisez prend en charge l’utilisation de dossiers de résultats de recherche, appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer la **PR\_STORE_SUPPORT_MASK** propriété ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si l’indicateur STORE_SEARCH_OK est défini, la recherche est pris en charge. Si elle n’est pas définie, vous aurez besoin d’une autre approche telles que l’inspection manuellement les dossiers cible.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Pour rechercher un ou plusieurs dossiers dans une banque de messages
  
1. Si vous disposez d’un dossier de résultats de recherche à partir d’une recherche précédente, passez à l’étape 2. Dans le cas contraire, pour créer un dossier de résultats de recherche :
    
    1. Récupérer l’identificateur d’entrée pour le dossier racine de résultats de recherche à l’appel de méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages et demande **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).
        
    2. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir le dossier représenté par PR_FINDER_ENTRYID. 
        
    3. Appeler la méthode de [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) du dossier pour créer un dossier de résultats de recherche avec l’indicateur FOLDER_SEARCH. 
    
2. Créer une restriction pour stocker vos critères de recherche. 
    
3. Créer un tableau d’identificateurs d’entrée qui représentent les dossiers de recherche. Cette étape est inutile si le dossier de résultats de recherche n’a été utilisé et que vous souhaitez les mêmes dossiers de recherche.
    
4. Appelez méthode pointant _lpContainerList_ sur le tableau d’identificateur de l’entrée et _lpRestriction_ à la restriction [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier de résultats de recherche. 
    
5. Si vous avez enregistré les notifications complète de recherche avec la banque de messages, attendez que la notification d’arriver.
    
6. Afficher les résultats de la recherche par la méthode les résultats de recherche du dossier [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pour accéder à sa table de contenu. 
    
7. Appelez le contenu [IMAPITable::QueryRows](imapitable-queryrows.md) méthode table pour récupérer les messages qui satisfont les critères de recherche. 
    

