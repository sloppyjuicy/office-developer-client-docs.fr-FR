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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316316"
---
# <a name="pidtagfoldertype-canonical-property"></a>Propriété canonique PidTagFolderType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une constante qui indique le type de dossier. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLDER_TYPE  <br/> |
|Identificateur :  <br/> |0x3601  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement l'une des valeurs suivantes:
  
FOLDER_GENERIC 
  
> Dossier générique contenant des messages et d'autres dossiers.
    
FOLDER_ROOT 
  
> Dossier racine de la table de hiérarchie des dossiers, c'est-à-dire un dossier qui n'a pas de dossier parent.
    
FOLDER_SEARCH 
  
> Dossier contenant les résultats d'une recherche, sous la forme de liens vers des messages qui répondent aux critères de recherche.
    
La racine d'un magasin de messages ne doit pas être confondue avec la racine de la sous-arborescence message interpersonne (IPM) dans cette banque. Le dossier racine de la Banque, qui n'a pas de parent, est obtenu en appelant la méthode [IMsgStore:: OpenEntry](imsgstore-openentry.md) avec un identificateur d'entrée null. Le dossier racine de la sous-arborescence IPM, qui a un parent, est obtenu à l'aide de la valeur de la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) pour l'appel **OpenEntry** . 
  
MAPI n'autorise qu'un seul dossier racine par Banque de messages. Ce dossier contient des messages et d'autres dossiers. La propriété **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) du dossier racine contient l'identificateur d'entrée propre au dossier.
  
Les informations contenues dans un dossier de résultats de recherche sont principalement stockées dans sa table des matières, qui contient les mêmes colonnes qu'une table de contenu classique, ainsi que deux colonnes supplémentaires identifiant le dossier dans lequel chaque message a été trouvé: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (nom complet, obligatoire) et cette propriété (identificateur d'entrée, facultatif).
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

