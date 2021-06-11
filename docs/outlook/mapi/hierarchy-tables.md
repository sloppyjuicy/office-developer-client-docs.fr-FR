---
title: Tables hiérarchiques
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
# <a name="hierarchy-tables"></a>Tables hiérarchiques

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de hiérarchie contient des informations sur les dossiers d’une magasin de messages ou sur les conteneurs d’un conteneur de carnet d’adresses. Chaque ligne d’une table hiérarchique contient un ensemble de colonnes contenant des informations sur un conteneur de dossier ou de carnet d’adresses. Les tables hiérarchiques sont principalement utilisées par les clients et implémentées par les fournisseurs de magasins de messages pour afficher une arborescence de dossiers et de sous-dossiers et implémentées par les fournisseurs de carnets d’adresses pour afficher une arborescence de conteneurs dans le carnet d’adresses. Les conteneurs qui ne peuvent pas contenir de sous-conteneurs, comme indiqué par l’absence de l’indicateur AB_SUBCONTAINERS dans leur propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags),](pidtagcontainerflags-canonical-property.md)n’implémentent pas de table hiérarchique.
  
Vous pouvez accéder à une table hiérarchique en appelant :
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Ou -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) passing **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) as the property tag and IID_IMAPITable as the interface identifier.
    
Les conteneurs et dossiers doivent prendre en charge les deux techniques d’extraction des propriétés de table. Il est inacceptable pour les fournisseurs de services de prendre en charge un seul moyen d’accéder à ces tables, car les clients s’attendent à avoir le choix. 
  
> [!IMPORTANT]
> Il n’est pas garanti que les fournisseurs du Store respectent l’ordre de tri spécifié pour les tables hiérarchiques. 
  
L’appel **à IMAPIProp::OpenProperty** implique d’accéder à la table de hiérarchie en ouvrant sa propriété correspondante, **PR_CONTAINER_HIERARCHY**. Bien **que PR_CONTAINER_HIERARCHY** ne puisse pas être récupéré par le biais de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) d’un dossier ou d’un conteneur, il est inclus dans le tableau de balises de propriétés renvoyé par la méthode [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_HIERARCHY** permet également d’inclure ou d’exclure une table hiérarchique d’une opération de copie. Si un client spécifie **PR_CONTAINER_HIERARCHY** dans le paramètre  *lpExcludeProps*  pour [IMAPIProp::CopyTo](imapiprop-copyto.md) dans une opération de copie, le nouveau dossier ou conteneur ne prendra pas en charge la table hiérarchique du dossier ou conteneur d’origine. 
  
Les propriétés suivantes définissent le jeu de colonnes requis dans un tableau hiérarchique :
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** contient le nom du conteneur ou du dossier qui doit apparaître dans l’affichage de la hiérarchie. 
  
 **PR_ENTRYID** est l’identificateur d’entrée associé à ce conteneur ou dossier. Il s’agit d’un identificateur d’entrée à long terme. Les clients et MAPI peuvent transmettre cet identificateur d’entrée à **OpenEntry** pour ouvrir le conteneur ou le dossier et afficher son contenu en appelant [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** est une valeur numérique qui indique le niveau de retrait pour ce conteneur ou ce dossier, zéro étant le niveau supérieur. Plus la hiérarchie d’un conteneur ou d’un dossier est profonde, plus la valeur de **sa propriété PR_DEPTH** est élevée. Les clients utilisent **la PR_DEPTH** pour afficher une table hiérarchique de manière appropriée afin que les utilisateurs voient clairement les relations parent et enfant. La profondeur du conteneur ou du dossier est toujours relative au conteneur ou au dossier implémentant la table de hiérarchie. 
  
 **PR_OBJECT_TYPE** est toujours définie sur MAPI_ABCONT pour les tables de hiérarchie de carnet d’adresses et MAPI_FOLDER pour les tables de hiérarchie de dossiers. 
  
 **PR_DISPLAY_TYPE** est une valeur numérique liée à l’affichage d’un conteneur ou d’un dossier dans la table hiérarchique. Il est principalement utilisé à des fins d’affichage, pour différencier visuellement les types de conteneurs ou de dossiers. De nombreux fournisseurs de magasins de messages et de carnets d’adresses utilisent des icônes pour les différents types d’affichage. C’est au fournisseur de fournir ces icônes . MAPI ne fournit pas les valeurs par défaut. 
  
MAPI définit de nombreuses valeurs pour **PR_DISPLAY_TYPE**, certaines valides pour les dossiers et d’autres qui sont utilisées avec les tables hiérarchiques des conteneurs de carnet d’adresses. En règle générale, **l’PR_DISPLAY_TYPE** d’un dossier est définie sur DT_FOLDER pour indiquer une icône de dossier par défaut, une DT_FOLDER_LINK pour indiquer une icône qui représente un lien vers un autre dossier ou une DT_FOLDER_SPECIAL pour indiquer une icône propre à l’application. DT_FOLDER_LINK est utilisé avec les dossiers de résultats de recherche. 
  
Outre ces colonnes requises, les tables de hiérarchie de carnet d’adresses doivent inclure la PR_CONTAINER_FLAGS de carnet **d’adresses.** **PR_CONTAINER_FLAGS** différents attributs sur un conteneur dans la hiérarchie et est utilisé pour distinguer un conteneur d’un autre. 
  
Une propriété facultative pour les tables de hiérarchie de carnet d’adresses est **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Les tables de hiérarchie de magasin de messages incluent ces propriétés dans leur ensemble de colonnes requis :
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Les fournisseurs de carnets d’adresses doivent prendre en charge les méthodes **IMAPITable** suivantes dans leurs implémentations de table hiérarchique, car elles sont requises par le carnet d’adresses intégré MAPI : 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

