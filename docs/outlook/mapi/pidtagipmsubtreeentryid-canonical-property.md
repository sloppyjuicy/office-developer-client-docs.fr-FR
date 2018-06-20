---
title: Propriété canonique PidTagIpmSubtreeEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9635c06ffa5638e370312e3b2b29e0c98161a766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786143"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a>Propriété canonique PidTagIpmSubtreeEntryId

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur d’entrée de la racine de la sous-arborescence de dossier message interpersonnel (IPM) dans l’arborescence de dossiers de la banque de messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IPM_SUBTREE_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E0  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété représente la racine de la hiérarchie IPM. Clients IPM ne doivent pas afficher tous les dossiers qui ne sont pas des sous-dossiers du dossier représenté par cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

