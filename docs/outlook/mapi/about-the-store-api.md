---
title: À propos de l’API du magasin
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 31aff61ec5868b0f1e9ab34d498b2e8175519f0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782877"
---
# <a name="about-the-store-api"></a>À propos de l’API du magasin

  
  
**S’applique à**: Outlook 
  
L’API stocker fournit la fonctionnalité de magasin de divers pour stocker les fournisseurs. Il fournit les définitions, types de données, propriétés et interfaces suivantes.
  
Définitions :
  
- [Constantes pour l’API du magasin](mapi-constants.md)
    
Types de données :
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propriétés nommées :
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Afficher les tailles de dossier de serveur](display-server-folder-sizes-property.md)**
    
- **[Masquer l’Option de mise à jour de réunion](hide-meeting-update-option-property.md)**
    
- **[Magasin de marque Type privé](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Fournisseurs de magasins qui ne nécessitent pas une des fonctionnalités offertes par ces propriétés nommées peuvent simplement les ignorer et implémenter pas prise en charge dans l’interface **IMAPIProp** . Étant donné que ces propriétés sont fournies à partir de Microsoft Outlook 2003 Service Pack 1, en les ajoutant à un magasin dans une version antérieure de Microsoft Outlook n’a aucun effet. Ils sont ignorés s’ils n’existent pas ou si sa valeur est **false**. 
  
Propriétés :
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Interfaces :
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Inscription des magasins pour l’indexation

Le Gestionnaire de protocole MAPI vérifie le Registre Windows pour les magasins il doit indexer à des fins de recherche. Fournisseurs de magasins indexer doivent être enregistrés dans le Registre Windows. Pour plus d’informations sur l’inscription des fournisseurs de magasins pour l’indexation dans Outlook 2013 ou Outlook 2010, voir [Sur inscription magasins pour l’indexation](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>L’indexation des magasins

Fournisseurs de magasins MAPI peuvent choisir d’autoriser le Gestionnaire de protocole MAPI pour analyser et indexer les messages dans le magasin, ou envoyer des notifications à l’indexeur que s’il existe des messages à indexer. Pour plus d’informations sur l’indexation basée sur les notifications, voir [L’indexation du magasin About Notification-Based](about-notification-based-store-indexing.md).
  

