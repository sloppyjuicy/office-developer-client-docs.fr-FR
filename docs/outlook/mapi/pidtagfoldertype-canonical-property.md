---
title: Propriété canonique PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8d6167a7a3c983171f2ff9cb2a54c879a14dca0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591414"
---
# <a name="pidtagfoldertype-canonical-property"></a>Propriété canonique PidTagFolderType

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une constante qui indique le type de dossier. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLDER_TYPE  <br/> |
|Identificateur :  <br/> |0x3601  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement une des valeurs suivantes :
  
FOLDER_GENERIC 
  
> Un dossier générique qui contient des messages et autres dossiers.
    
FOLDER_ROOT 
  
> Le dossier racine de la table de hiérarchie de dossier, autrement dit, un dossier qui n’a aucun dossier parent.
    
FOLDER_SEARCH 
  
> Un dossier qui contient les résultats d’une recherche, sous la forme de liens vers les messages qui répondent aux critères de recherche.
    
La racine d’une banque de messages ne doit pas être confondue avec la racine de la sous-arborescence message interpersonnel (IPM) de cette banque. Dossier racine de la banque, qui n’a pas de parent, est obtenu en appelant la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec un identificateur d’entrée null. Dossier racine de la sous-arborescence IPM, qui a un parent, est obtenue à l’aide de la valeur de la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) pour l’appel de **OpenEntry** . 
  
MAPI ne permet qu’un seul dossier racine par banque de messages. Ce dossier contient des messages et autres dossiers. Propriété de **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) du dossier racine contient l’identificateur d’entrée du dossier.
  
Les informations contenues dans un dossier de résultats de recherche sont principalement stockés dans sa table des matières, qui contient les mêmes colonnes sous forme de tableau de type de contenu, ainsi que deux colonnes supplémentaires qui identifie le dossier dans lequel chaque message a été trouvé : **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (affiche le nom, requis) et que cette propriété (identificateur d’entrée, facultatif).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

