---
title: Propriété canonique PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 411adc200d4b337eaaa6b51e47269c0f02d9b899
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624495"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Propriété canonique PidTagServiceExtraUids

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste de structures [MAPIUID](mapiuid.md) qui identifient des sections de profil supplémentaires pour le service de message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Identificateur :  <br/> |0x3D0D  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

De nouvelles sections de profil peuvent être créées pour chaque filtre de message. Lorsque les informations sur le service de message doivent être copiées dans un autre profil, il est important de copier également les sections de profil supplémentaires pour les filtres. Un fournisseur de services qui utilise des sections de profil supplémentaires peut stocker les structures **MAPIUID** de ces sections de profil dans **PR_SERVICE_EXTRA_UIDS**, ce qui permet à MAPI de copier les informations de service de message supplémentaires.
  
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

