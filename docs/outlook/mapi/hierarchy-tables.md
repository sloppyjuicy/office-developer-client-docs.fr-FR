---
title: Tables de hiérarchies
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d135e0c224866cd2a675df2ef9ec1b206f3169ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580753"
---
# <a name="hierarchy-tables"></a>Tables de hiérarchies

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une table de hiérarchie contient des informations sur les dossiers dans une banque de messages ou les conteneurs dans un conteneur de carnet d’adresses. Chaque ligne d’une table de hiérarchie contient un ensemble de colonnes avec des informations sur un dossier ou le conteneur de carnet d’adresses. Tables de hiérarchie sont principalement utilisés par les clients et implémentés par les fournisseurs de banque de message pour afficher une arborescence de dossiers et les sous-dossiers et par les fournisseurs de carnet d’adresses pour afficher une arborescence de conteneurs dans le carnet d’adresses. Conteneurs qui ne peut pas contenir les sous-conteneurs, comme indiqué par l’absence de l’indicateur AB_SUBCONTAINERS dans leur propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), n’implémentent pas une table de hiérarchie.
  
Une table de hiérarchie est accessible en appelant :
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Ou -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en passant **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), ainsi que la balise de propriété IID_IMAPITable en tant que l’identificateur d’interface.
    
Conteneurs et dossiers doivent prendre en charge les deux méthodes pour récupérer les propriétés du tableau. N’est pas acceptable pour les fournisseurs de service prendre en charge qu’une seule manière d’accéder à ces tables, car les clients s’attendent à avoir le choix. 
  
> [!IMPORTANT]
> Fournisseurs de magasins ne sont pas garantis de respecter l’ordre de tri spécifié pour les tables de hiérarchie. 
  
L’appel vers **IMAPIProp::OpenProperty** implique l’accès à la table de hiérarchie en ouvrant sa propriété correspondante, **PR_CONTAINER_HIERARCHY**. Bien que **PR_CONTAINER_HIERARCHY** ne peut pas être récupéré à un dossier ou du conteneur [IMAPIProp::GetProps](imapiprop-getprops.md) , il est inclus dans le tableau de balise de propriété qui est retourné par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_HIERARCHY** peut également servir à inclure ou exclure d’une table de hiérarchie à partir d’une opération de copie. Si un client spécifie **PR_CONTAINER_HIERARCHY** dans le paramètre *lpExcludeProps* pour [IMAPIProp::CopyTo](imapiprop-copyto.md) dans une opération de copie, le nouveau dossier ou le conteneur ne prendra pas en charge la table de hiérarchie du dossier d’origine ou du conteneur. 
  
Les propriétés suivantes constituent la colonne dans une table de hiérarchie requise :
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** contient le nom pour le conteneur ou le dossier qui doit apparaître dans l’affichage de la hiérarchie. 
  
 **PR_ENTRYID** est l’identificateur d’entrée associé à ce conteneur ou d’un dossier. Il est supposé être un identificateur d’entrée à long terme. Clients et MAPI peuvent passer cet identificateur d’entrée à **OpenEntry** pour ouvrir le conteneur ou le dossier et afficher son contenu en appelant [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** est une valeur numérique qui indique le niveau de retrait de ce conteneur ou d’un dossier à zéro en cours de niveau supérieur. Plus la profondeur de la hiérarchie d’un conteneur ou un dossier se trouve, plus la valeur de sa propriété **PR_DEPTH** . Clients utilisent la propriété **PR_DEPTH** pour afficher une table de hiérarchie appropriée afin que les utilisateurs peuvent voir clairement les relations parent-enfant. Profondeur de conteneur ou de dossier est toujours par rapport au conteneur ou l’implémentation de la table de hiérarchie de dossier. 
  
 **PR_OBJECT_TYPE** est toujours définie sur MAPI_ABCONT pour les tables de hiérarchie adresse livre et MAPI_FOLDER pour les tables de hiérarchie de dossier. 
  
 **PR_DISPLAY_TYPE** est une valeur numérique qui se rapporte à la façon dont un conteneur ou un dossier s’affiche dans la table de hiérarchie. Il est principalement utilisé à des fins d’affichage, pour différencier visuellement les types de conteneurs ou de dossiers. Message de stocker et adresses fournisseurs livre utiliser des icônes pour les types d’affichage différents. Il est le fournisseur peut fournir ces icônes ; MAPI ne fournit pas de valeurs par défaut. 
  
MAPI définit plusieurs valeurs pour **PR_DISPLAY_TYPE**certains qui sont valides pour les dossiers et d’autres personnes qui sont utilisés avec les tables de hiérarchie de conteneurs de carnet d’adresses. En règle générale, **PR_DISPLAY_TYPE d’un dossier** a la valeur DT_FOLDER pour indiquer une icône de dossier par défaut, pour indiquer une icône qui représente un lien vers un autre dossier DT_FOLDER_LINK ou DT_FOLDER_SPECIAL pour indiquer l’icône qui est spécifique à l’application. DT_FOLDER_LINK est utilisé avec les dossiers de résultats de recherche. 
  
Outre ces colonnes obligatoires, tables de hiérarchie livre adresse doivent inclure la propriété **PR_CONTAINER_FLAGS** . **PR_CONTAINER_FLAGS** indique divers attributs sur un conteneur dans la hiérarchie et est utilisé pour distinguer un conteneur d’un autre. 
  
Propriété facultative pour les tables de hiérarchie adresse téléchargeable est la propriété **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Tables de hiérarchie de message-store incluent ces propriétés dans leur ensemble de colonnes requises :
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Fournisseurs de carnet d’adresses doivent prendre en charge les méthodes **IMAPITable** suivantes dans leurs implémentations de table de hiérarchie car ils sont requis par le carnet d’adresses intégré de MAPI : 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

