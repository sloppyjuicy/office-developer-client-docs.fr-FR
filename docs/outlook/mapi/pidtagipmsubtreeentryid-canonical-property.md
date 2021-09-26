---
title: Propriété canonique PidTagIpmSubtreeEntryId
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9a68227c61abe65f785739e42a2d09a01ba6ef3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583400"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a>Propriété canonique PidTagIpmSubtreeEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de la racine de la sous-arborescence du dossier de message interpersonnel (IPM) dans l’arborescence de dossiers de la magasin de messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IPM_SUBTREE_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E0  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété représente la racine de la hiérarchie IPM. Les clients IPM ne doivent pas afficher les dossiers qui ne sont pas des sous-dossiers du dossier représenté par cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

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

