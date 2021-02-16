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
# <a name="about-the-store-api"></a>À propos de l’API de magasin

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API Store fournit diverses fonctionnalités du Store aux fournisseurs de magasins. Il fournit les définitions, types de données, propriétés et interfaces suivants.
  
Définitions :
  
- [Constantes de l’API du Store](mapi-constants.md)
    
Types de données :
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propriétés nommées :
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Tailles des dossiers du serveur d’affichage](display-server-folder-sizes-property.md)**
    
- **[Masquer l’option de mise à jour de réunion](hide-meeting-update-option-property.md)**
    
- **[Rendre privé le type de magasin](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Les fournisseurs de magasins qui ne nécessitent aucune des fonctionnalités offertes par ces propriétés nommées peuvent simplement les ignorer et ne pas implémenter la prise en charge dans l’interface **IMAPIProp.** Étant donné que ces propriétés sont fournies à partir de Microsoft Outlook 2003 Service Pack 1, leur ajout à un magasin dans une version antérieure de Microsoft Outlook n’a aucun effet. Ils sont ignorés s’ils n’existent pas ou si leur valeur est **false**. 
  
Propriétés :
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Interfaces :
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Inscription de magasins pour l’indexation

Le handler de protocole MAPI vérifie dans le Registre Windows les magasins qu’il doit indexer à des fins de recherche. Les fournisseurs du Windows Store qui souhaitent être indexés doivent être inscrits dans le Registre Windows. Pour plus d’informations sur l’inscription de fournisseurs de magasins pour l’indexation dans Outlook 2013 ou Outlook 2010, voir à propos de l’inscription des magasins pour [l’indexation.](about-registering-stores-for-indexing.md)
  
## <a name="indexing-stores"></a>Magasins d’indexation

Les fournisseurs de magasins MAPI peuvent choisir d’autoriser le handler de protocole MAPI à analyser et indexer des messages dans la boutique, ou d’envoyer des notifications à l’indexeur uniquement lorsqu’il existe des messages à indexer. Pour plus d’informations sur l’indexation basée sur les notifications, voir à propos [Notification-Based'indexation dans le Store.](about-notification-based-store-indexing.md)
  

