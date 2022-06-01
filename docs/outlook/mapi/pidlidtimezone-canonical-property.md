---
title: Propriété canonique PidLidTimeZone
description: Décrit la propriété canonique PidLidTimeZone, qui spécifie des informations sur le fuseau horaire d’une réunion périodique.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
ms.openlocfilehash: 2d4e4c06c88ce99bb6aa221c0851e72ef76bd70e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811948"
---
# <a name="pidlidtimezone-canonical-property"></a>Propriété canonique PidLidTimeZone

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie des informations sur le fuseau horaire d’une réunion périodique.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |LID_TIME_ZONE  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Meeting  <br/> |
|ID long (LID) :  <br/> |0x0000000C  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est lue uniquement si la propriété **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) n’est pas définie, mais si la propriété **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) est TRUE et si la propriété **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) est FALSE. Le word inférieur spécifie un index dans une table qui contient des informations de fuseau horaire. Dans le word supérieur, seul le bit le plus élevé est lu. Si ce bit est défini, le fuseau horaire référencé n’observera pas l’heure d’été (DST), sinon les dates DST détaillées dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) seront suivies. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

