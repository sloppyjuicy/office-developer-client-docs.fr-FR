---
title: Propriété canonique PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 295b20ebc0c41104a8b1c8e46e2064c3ef32f99e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786486"
---
# <a name="pidtagpstpathhint-canonical-property"></a>Propriété canonique PidTagPstPathHint

  
  
**S’applique à**: Outlook 
  
Fournit le nom de table (fichier .pst) stockage personnel, l’utilisateur peut modifier, pour la boîte de dialogue de configuration. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W  <br/> |
|Identificateur :  <br/> |0x6771  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Tableau de stockage personnel (.pst) interne  <br/> |
   
## <a name="remarks"></a>Remarques

Si la propriété **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) est utilisée au lieu de cela, la boîte de dialogue configuration s’ouvre, mais l’utilisateur n’est pas être autorisé pour modifier le chemin d’accès et de nombreuses autres propriétés.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]] 
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

