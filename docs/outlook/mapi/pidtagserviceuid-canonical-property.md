---
title: Propriété canonique PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: Contient la structure d’un service de message. Cette propriété est calculée par MAPI sur les objets de section de profil. MAPI l’utilise pour grouper des fournisseurs.
ms.openlocfilehash: 0964f93dcc5caed278c385dcc3644fea428b36b9
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405082"
---
# <a name="pidtagserviceuid-canonical-property"></a>Propriété canonique PidTagServiceUid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la structure [MAPIUID](mapiuid.md) pour un service de message. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_UID  <br/> |
|Identificateur :  <br/> |0x3D0C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par MAPI sur les objets de section de profil. MAPI l’utilise pour grouper tous les fournisseurs qui appartiennent au même service de messagerie. Cette propriété est fournie en tant que paramètre pour la plupart des méthodes [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Elle ne doit pas apparaître dans Mapisvc.inf. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

