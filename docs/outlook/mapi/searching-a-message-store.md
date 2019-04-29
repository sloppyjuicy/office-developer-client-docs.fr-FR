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
# <a name="searching-a-message-store"></a>Recherche d’un message dans une banque

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes peuvent effectuer des recherches dans un ou plusieurs dossiers à la recherche de messages qui correspondent aux critères de recherche. La technique de recherche la plus simple consiste à appliquer une restriction pour définir des critères et à placer les résultats dans un dossier de résultats de recherche, créé explicitement pour cette recherche ou pour une recherche préalable. Toutes les banques de messages ne prennent pas en charge cette technique. 

Pour déterminer si la Banque de messages que vous utilisez prend en charge à l'aide des dossiers de résultats de recherche, appelez sa méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) pour récupérer la propriété **\_PR STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si l'indicateur STORE_SEARCH_OK est défini, la recherche est prise en charge. Si ce n'est pas le cas, vous aurez besoin d'une autre approche, telle que l'inspection manuelle des dossiers cibles.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Pour rechercher un ou plusieurs dossiers dans une banque de messages
  
1. Si vous disposez d'un dossier Search-Results d'une recherche précédente, passez à l'étape 2. Dans le cas contraire, pour créer un dossier de résultats de recherche, procédez comme suit:
    
    1. Récupérez l'identificateur d'entrée pour le dossier racine de résultats de recherche en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages et en demandant **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).
        
    2. Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) pour ouvrir le dossier représenté par PR_FINDER_ENTRYID. 
        
    3. Appelez la méthode [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) pour créer un dossier de résultats de recherche avec l'indicateur FOLDER_SEARCH défini. 
    
2. Créez une restriction pour conserver vos critères de recherche. 
    
3. Créez un tableau d'identificateurs d'entrée qui représentent les dossiers à rechercher. Cette étape n'est pas nécessaire si le dossier Search-Results a été utilisé avant et que vous souhaitez effectuer des recherches dans les mêmes dossiers.
    
4. Appelez la méthode [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier Search-Results, puis pointez _lpContainerList_ vers le tableau de l'identificateur d'entrée et _lpRestriction_ à la restriction. 
    
5. Si vous vous êtes inscrit pour les notifications d'exécution de la recherche avec la Banque de messages, patientez jusqu'à ce que la notification arrive.
    
6. Affichez les résultats de la recherche en appelant la méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) du dossier Search-Results pour accéder à sa table des matières. 
    
7. Appelez la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire les messages qui satisfont les critères de recherche. 
    

