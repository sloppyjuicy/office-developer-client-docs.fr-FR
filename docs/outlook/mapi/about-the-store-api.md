---
title: À propos de l’API de magasin
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321748"
---
# <a name="about-the-store-api"></a>À propos de l’API de magasin

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'API Store fournit des fonctionnalités de magasin pour stocker les fournisseurs. Il fournit les defintions, les types de données, les propriétés et les interfaces suivants.
  
Définitions :
  
- [Constantes pour l'API Store](mapi-constants.md)
    
Types de données:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propriétés nommées:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Afficher les tailles de dossier des serveurs](display-server-folder-sizes-property.md)**
    
- **[Masquer l'option de mise à jour de réunion](hide-meeting-update-option-property.md)**
    
- **[Définir le type de magasin comme privé](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Les fournisseurs de banque qui ne nécessitent aucune des fonctionnalités offertes par ces propriétés nommées peuvent simplement les ignorer et ne pas implémenter la prise en charge dans l'interface **IMAPIProp** . Étant donné que ces propriétés sont fournies à partir de Microsoft Outlook 2003 Service Pack 1, leur ajout à un magasin dans une version antérieure de Microsoft Outlook n'a aucun effet. Elles sont ignorées si elles n'existent pas ou si leur valeur **** est false. 
  
Propriétés :
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Interfaces :
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Enregistrement des magasins pour l'indexation

Le gestionnaire de protocole MAPI vérifie si le Registre Windows contient des magasins qu'il doit indexer à des fins de recherche. Les fournisseurs de banque qui souhaitent être indexés doivent être enregistrés dans le Registre Windows. Pour plus d'informations sur l'inscription des fournisseurs de magasin pour l'indexation dans Outlook 2013 ou Outlook 2010, consultez la rubrique [à propos de l'inscription de magasins pour l'indexation](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Indexation des magasins

Les fournisseurs de magasins MAPI peuvent choisir d'autoriser le gestionnaire de protocole MAPI à analyser et indexer les messages de la Banque, ou d'envoyer des notifications à l'indexeur uniquement lorsqu'il y a des messages à indexer. Pour plus d'informations sur l'indexation basée sur les notifications, consultez la rubrique [à propos de l'indexation du magasin basé sur les notifications](about-notification-based-store-indexing.md).
  

