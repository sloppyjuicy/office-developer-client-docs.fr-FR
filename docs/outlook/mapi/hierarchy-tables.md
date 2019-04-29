---
title: Tables de hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428367"
---
# <a name="hierarchy-tables"></a>Tables de hiérarchie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de hiérarchie contient des informations sur les dossiers d'une banque de messages ou sur les conteneurs d'un conteneur de carnet d'adresses. Chaque ligne d'une table de hiérarchie contient un ensemble de colonnes contenant des informations sur un conteneur de dossier ou de carnet d'adresses. Les tables de hiérarchie sont principalement utilisées par les clients et mises en œuvre par les fournisseurs de banques de messages pour afficher une arborescence de dossiers et de sous-dossiers et mises en œuvre par les fournisseurs de carnet d'adresses pour afficher une arborescence de conteneurs dans le carnet d'adresses. Les conteneurs qui ne peuvent pas contenir de sous-conteneurs, comme indiqué par l'absence de l'indicateur AB_SUBCONTAINERS dans leur propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), n'implémentent pas de table de hiérarchie.
  
Il est possible d'accéder à une table de hiérarchie en appelant:
  
- [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Des
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) passant **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) en tant que balise de propriété et IID_IMAPITable comme identificateur d'interface.
    
Les conteneurs et les dossiers doivent prendre en charge les deux techniques de récupération des propriétés de table. Il est inacceptable que les fournisseurs de services ne prennent en charge qu'une seule méthode pour accéder à ces tables, car les clients s'attendent à avoir le choix. 
  
> [!IMPORTANT]
> Il n'est pas garanti que les fournisseurs de magasins respectent l'ordre de tri défini pour les tables de hiérarchie. 
  
L'appel à **IMAPIProp:: OpenProperty** implique l'accès à la table de hiérarchie en ouvrant sa propriété correspondante, **PR_CONTAINER_HIERARCHY**. Bien que **PR_CONTAINER_HIERARCHY** ne puisse pas être récupéré par le biais de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) d'un dossier ou d'un conteneur, il est inclus dans le tableau des balises de propriété qui est renvoyé par la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_HIERARCHY** peut également être utilisé pour inclure ou exclure une table de hiérarchie d'une opération de copie. Si un client spécifie **PR_CONTAINER_HIERARCHY** dans le paramètre *lpExcludeProps* pour [IMAPIProp:: CopyTo](imapiprop-copyto.md) dans une opération de copie, le nouveau dossier ou conteneur ne prend pas en charge la table de hiérarchie du dossier ou du conteneur d'origine. 
  
Les propriétés suivantes constituent le jeu de colonnes obligatoire dans une table de hiérarchie:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** contient le nom du conteneur ou du dossier qui doit apparaître dans l'affichage de la hiérarchie. 
  
 **PR_ENTRYID** est l'identificateur d'entrée associé à ce conteneur ou dossier. Il s'agit normalement d'un identificateur d'entrée à long terme. Les clients et MAPI peuvent transmettre cet identificateur d'entrée à **OpenEntry** pour ouvrir le conteneur ou le dossier et afficher son contenu en appelant [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** est une valeur numérique qui indique le niveau de retrait de ce conteneur ou dossier dont le niveau supérieur est zéro. Plus profond dans la hiérarchie d'un conteneur ou d'un dossier, plus la valeur de sa propriété **PR_DEPTH** est élevée. Les clients utilisent la propriété **PR_DEPTH** pour afficher une table hiérarchique de manière appropriée afin que les utilisateurs puissent voir clairement les relations parent et enfant. La profondeur du conteneur ou du dossier est toujours relative au conteneur ou au dossier qui implémente la table de hiérarchie. 
  
 **PR_OBJECT_TYPE** est toujours défini sur MAPI_ABCONT pour les tables de hiérarchie de carnet d'adresses et MAPI_FOLDER pour les tables de hiérarchie de dossiers. 
  
 **PR_DISPLAY_TYPE** est une valeur numérique qui correspond à la façon dont un conteneur ou un dossier est affiché dans la table de hiérarchie. Il est principalement utilisé à des fins d'affichage, afin de se différencier visuellement entre les types de conteneurs ou de dossiers. De nombreux fournisseurs de banques de messages et de carnets d'adresses utilisent des icônes pour les différents types d'affichage. Il revient au fournisseur de fournir ces icônes; MAPI ne fournit pas de valeurs par défaut. 
  
MAPI définit de nombreuses valeurs pour **PR_DISPLAY_TYPE**, certaines sont valides pour les dossiers et d'autres qui sont utilisés avec les tables de hiérarchie des conteneurs du carnet d'adresses. En règle générale, le **PR_DISPLAY_TYPE** d'un dossier est défini sur DT_FOLDER pour indiquer une icône de dossier par défaut, DT_FOLDER_LINK pour indiquer une icône qui représente un lien vers un autre dossier ou DT_FOLDER_SPECIAL pour indiquer une icône qui est propre à l'application. DT_FOLDER_LINK est utilisé avec les dossiers de résultats de recherche. 
  
En plus de ces colonnes obligatoires, les tables de hiérarchie des carnets d'adresses doivent inclure la propriété **PR_CONTAINER_FLAGS** . **PR_CONTAINER_FLAGS** indique différents attributs concernant un conteneur dans la hiérarchie et est utilisé pour différencier un conteneur d'un autre. 
  
Une propriété facultative pour les tables de hiérarchie de carnets d'adresses est la propriété **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Les tables de hiérarchie de magasin de messages incluent ces propriétés dans leur jeu de colonnes obligatoire:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Les fournisseurs de carnets d'adresses doivent prendre en charge les méthodes **IMAPITable** suivantes dans leurs implémentations de table de hiérarchie car elles sont requises par le carnet d'adresses intégré MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

