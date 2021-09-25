---
title: Propriété canonique PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e2407a9efdf43a7a83418e1ab77e1054ac3b954b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574796"
---
# <a name="pidtagpstpathhint-canonical-property"></a>Propriété canonique PidTagPstPathHint

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit le nom de la table de stockage personnel (fichier .pst), que l’utilisateur peut modifier, pour la boîte de dialogue de configuration. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W  <br/> |
|Identificateur :  <br/> |0x6771  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Table de stockage personnel (.pst) interne  <br/> |
   
## <a name="remarks"></a>Remarques

Si la **propriété PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) est utilisée à la place, la boîte de dialogue de configuration s’ouvre, mais l’utilisateur n’est pas autorisé à modifier le chemin d’accès et de nombreuses autres propriétés.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]] 
  
> Fournit des références aux spécifications Exchange Server protocole.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

