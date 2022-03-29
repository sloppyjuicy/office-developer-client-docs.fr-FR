---
title: Propriété canonique PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a8537c2d7afbf4c1467ec7381131d0f3f832dea5
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455299"
---
# <a name="pidtagfoldertype-canonical-property"></a>Propriété canonique PidTagFolderType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une constante qui indique le type de dossier. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLDER_TYPE  <br/> |
|Identificateur :  <br/> |0x3601  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement l’une des valeurs suivantes :
  
FOLDER_GENERIC 
  
> Dossier générique qui contient des messages et d’autres dossiers.
    
FOLDER_ROOT 
  
> Dossier racine de la table de hiérarchie de dossiers, c’est-à-dire un dossier qui n’a pas de dossier parent.
    
FOLDER_SEARCH 
  
> Dossier qui contient les résultats d’une recherche, sous la forme de liens vers des messages qui répondent aux critères de recherche.
    
La racine d’une magasin de messages ne doit pas être confondue avec la racine de la sous-arbre de message interpersonnel (IPM) de ce magasin. Le dossier racine de la boutique, qui n’a aucun parent, est obtenu en appelant la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec un identificateur d’entrée null. Le dossier racine de la sous-arbre IPM, qui a un parent, est obtenu à l’aide de la valeur de la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) pour l’appel **OpenEntry** . 
  
MAPI n’autorise qu’un dossier racine par magasin de messages. Ce dossier contient des messages et d’autres dossiers. La propriété **PR_PARENT_ENTRYID racine (**[PidTagParentEntryId](pidtagparententryid-canonical-property.md)) contient le propre identificateur d’entrée du dossier.
  
Les informations d’un dossier de résultats de recherche sont principalement stockées dans sa table des matières, qui contient les mêmes colonnes qu’une table de contenu classique, ainsi que deux colonnes supplémentaires identifiant le dossier dans lequel chaque message a été trouvé : **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (nom complet, obligatoire) et cette propriété (identificateur d’entrée, facultatif).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

