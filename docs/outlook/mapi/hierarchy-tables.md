---
title: Tables de hiérarchie
description: Une table de hiérarchie contient des informations sur les dossiers d’un magasin de messages ou les conteneurs d’un conteneur de carnet d’adresses.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
ms.openlocfilehash: b16861bed79f21d58fe87312a9d30d6c2fba177f
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816933"
---
# <a name="hierarchy-tables"></a>Tables de hiérarchie
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de hiérarchie contient des informations sur les dossiers d’un magasin de messages ou les conteneurs d’un conteneur de carnet d’adresses. Chaque ligne d’une table de hiérarchie contient un ensemble de colonnes contenant des informations sur un dossier ou un conteneur de carnet d’adresses. Les tables hiérarchiques sont principalement utilisées par les clients et implémentées par les fournisseurs de magasins de messages pour afficher une arborescence de dossiers et de sous-dossiers et implémentées par les fournisseurs de carnets d’adresses pour afficher une arborescence de conteneurs dans le carnet d’adresses. Les conteneurs qui ne peuvent pas contenir de sous-conteneurs, comme indiqué par l’absence de l’indicateur AB_SUBCONTAINERS dans leur propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), n’implémentent pas de table de hiérarchie.
  
Une table de hiérarchie est accessible en appelant :
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).

    - Ou -

- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) passant **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) comme balise de propriété et IID_IMAPITable comme identificateur d’interface.

Les conteneurs et les dossiers doivent prises en charge les deux techniques pour récupérer les propriétés de la table. Il est inacceptable que les fournisseurs de services prennent en charge une seule façon d’accéder à ces tables, car les clients s’attendent à avoir le choix. 
  
> [!IMPORTANT]
> Il n’est pas garanti que les fournisseurs de magasin respectent le jeu d’ordres de tri spécifié pour les tables de hiérarchie.
  
L’appel à **IMAPIProp::OpenProperty** implique d’accéder à la table de hiérarchie en ouvrant sa propriété correspondante, **PR_CONTAINER_HIERARCHY**. Bien que **PR_CONTAINER_HIERARCHY** ne puisse pas être récupérée via la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) d’un dossier ou d’un conteneur, elle est incluse dans le tableau de balises de propriétés retourné par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) .
  
 **PR_CONTAINER_HIERARCHY** peut également être utilisé pour inclure ou exclure une table de hiérarchie d’une opération de copie. Si un client spécifie **PR_CONTAINER_HIERARCHY** dans le paramètre *lpExcludeProps* pour [IMAPIProp::CopyTo](imapiprop-copyto.md) dans une opération de copie, le nouveau dossier ou conteneur ne prend pas en charge la table hiérarchique du dossier ou du conteneur d’origine.
  
Les propriétés suivantes constituent l’ensemble de colonnes requis dans une table de hiérarchie :
  
||Valeur |
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** contient le nom du conteneur ou du dossier qui doit apparaître dans l’affichage de la hiérarchie.
  
 **PR_ENTRYID** est l’identificateur d’entrée associé à ce conteneur ou dossier. Il doit s’agir d’un identificateur d’entrée à long terme. Les clients et MAPI peuvent passer cet identificateur d’entrée à **OpenEntry** pour ouvrir le conteneur ou le dossier et afficher son contenu en appelant [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
  
 **PR_DEPTH** est une valeur numérique qui indique le niveau de mise en retrait pour ce conteneur ou dossier, zéro étant le niveau supérieur. Plus un conteneur ou un dossier réside dans la hiérarchie, plus la valeur de sa propriété **PR_DEPTH** est élevée. Les clients utilisent la propriété **PR_DEPTH** pour afficher une table de hiérarchie de manière appropriée afin que les utilisateurs puissent voir clairement les relations parent-enfant. La profondeur du conteneur ou du dossier est toujours relative au conteneur ou au dossier qui implémente la table de hiérarchie.
  
 **PR_OBJECT_TYPE** est toujours définie sur MAPI_ABCONT pour les tables de hiérarchie de carnet d’adresses et MAPI_FOLDER pour les tables de hiérarchie de dossiers.
  
 **PR_DISPLAY_TYPE** est une valeur numérique liée à la façon dont un conteneur ou un dossier est affiché dans la table de hiérarchie. Il est principalement utilisé à des fins d’affichage, afin de différencier visuellement les types de conteneurs ou de dossiers. De nombreux fournisseurs de magasins de messages et de carnets d’adresses utilisent des icônes pour les différents types d’affichage. Il appartient au fournisseur de fournir ces icônes ; MAPI ne fournit pas les valeurs par défaut.
  
MAPI définit de nombreuses valeurs pour **PR_DISPLAY_TYPE**, certaines valides pour les dossiers et d’autres utilisées avec les tables hiérarchiques des conteneurs de carnets d’adresses. En règle générale, le **PR_DISPLAY_TYPE** d’un dossier est défini sur DT_FOLDER pour indiquer une icône de dossier par défaut, DT_FOLDER_LINK pour indiquer une icône qui représente un lien vers un autre dossier ou DT_FOLDER_SPECIAL pour indiquer une icône spécifique à l’application. DT_FOLDER_LINK est utilisé avec les dossiers de résultats de recherche.
  
En plus de ces colonnes requises, les tables de hiérarchie de carnet d’adresses doivent inclure la propriété **PR_CONTAINER_FLAGS** . **PR_CONTAINER_FLAGS** indique différents attributs sur un conteneur dans la hiérarchie et est utilisé pour distinguer un conteneur d’un autre.
  
Une propriété facultative pour les tables de hiérarchie de carnet d’adresses est la propriété **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Les tables de hiérarchie du magasin de messages incluent ces propriétés dans leur ensemble de colonnes requis :
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))

Les fournisseurs de carnets d’adresses doivent prendre en charge les méthodes **IMAPITable** suivantes dans leurs implémentations de table de hiérarchie, car elles sont requises par le carnet d’adresses intégré MAPI :
  
|Méthode |Méthode |
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |

## <a name="see-also"></a>Voir aussi

[MAPI Tables](mapi-tables.md)
