---
title: Propriété canonique PidTagIpmSubtreeEntryId
description: Décrit la propriété canonique PidTagIpmSubtreeEntryId, qui représente la racine de la hiérarchie IPM.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
ms.openlocfilehash: eae123b0f1c23f8cd6fe0ee0463f457ccdd329b8
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752245"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a>Propriété canonique PidTagIpmSubtreeEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de la racine de la sous-arborescence du dossier des messages interpersonnels (IPM) dans l’arborescence des dossiers du magasin de messages. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IPM_SUBTREE_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E0  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété représente la racine de la hiérarchie IPM. Les clients IPM ne doivent pas afficher de dossiers qui ne sont pas des sous-dossiers du dossier représenté par cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

