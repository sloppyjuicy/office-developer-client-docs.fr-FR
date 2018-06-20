---
title: Propriété canonique PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 71f802014200d4b767c346c14df53f1193d44b0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786783"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Propriété canonique PidTagServiceExtraUids

  
  
**S’applique à**: Outlook 
  
Contient une liste des structures [MAPIUID](mapiuid.md) qui identifient les sections de profil supplémentaires pour le service de message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Identificateur :  <br/> |0x3D0D  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Nouvelles sections profil peuvent être créées pour chaque filtre de message. Lorsque les informations sur le service de message doit être copié vers un autre profil, il est important de copier les sections de profil supplémentaires pour les filtres ainsi. Un fournisseur de services qui utilise des sections de profil supplémentaires peut stocker les structures **MAPIUID** de ces sections profil dans **PR_SERVICE_EXTRA_UIDS**, qui permet de MAPI copier les informations de service de message supplémentaire.
  
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

