---
title: À propos de l’API de magasin
description: L’API Store fournit diverses fonctionnalités de magasin pour les fournisseurs de stockage. Cet article décrit les définitions, types de données, propriétés et interfaces associés.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
ms.openlocfilehash: 6e66323a3c00ec32e37d99a51da6c1441423f6f3
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770025"
---
# <a name="about-the-store-api"></a>À propos de l’API de magasin

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API Store fournit diverses fonctionnalités de magasin pour les fournisseurs de stockage. Il fournit les définitions, types de données, propriétés et interfaces suivants.
  
Définitions :
  
- [Constantes pour l’API Store](mapi-constants.md)
    
Types de données :
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propriétés nommées :
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Afficher les tailles des dossiers du serveur](display-server-folder-sizes-property.md)**
    
- **[Masquer l’option De mise à jour de réunion](hide-meeting-update-option-property.md)**
    
- **[Rendre le type de magasin privé](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Les fournisseurs de magasins qui ne nécessitent aucune des fonctionnalités offertes par ces propriétés nommées peuvent simplement les ignorer et ne pas implémenter la prise en charge dans l’interface **IMAPIProp** . Étant donné que ces propriétés sont fournies à partir de Microsoft Outlook Service Pack 1 2003, leur ajout à un magasin dans une version antérieure de Microsoft Outlook n’a aucun effet. Ils sont ignorés s’ils n’existent pas ou si leur valeur est **false**. 
  
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

Le gestionnaire de protocole MAPI vérifie le registre Windows pour les magasins qu’il doit indexer à des fins de recherche. Les fournisseurs de magasins qui souhaitent être indexés doivent être inscrits dans le registre Windows. Pour plus d’informations sur l’inscription des fournisseurs de magasins pour l’indexation dans Outlook 2013 ou Outlook 2010, consultez [À propos de l’inscription des magasins pour l’indexation](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Magasins d’indexation

Les fournisseurs de magasin MAPI peuvent choisir d’autoriser le gestionnaire de protocole MAPI à analyser et à indexer les messages dans le magasin, ou d’envoyer des notifications à l’indexeur uniquement quand des messages doivent être indexés. Pour plus d’informations sur l’indexation basée sur les notifications, consultez [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).
  

