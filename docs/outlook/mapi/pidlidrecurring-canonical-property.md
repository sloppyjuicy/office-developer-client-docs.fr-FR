---
title: Propriété canonique PidLidRecurring
description: Décrit la propriété canonique PidLidRecurring, qui spécifie si un message de rendez-vous est récurrent.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
ms.openlocfilehash: 6f608efd9e15b732a01fe6d2e69585b5923b7e71
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816100"
---
# <a name="pidlidrecurring-canonical-property"></a>Propriété canonique PidLidRecurring

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si un message de rendez-vous est récurrent.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidRecurring  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008223  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est TRUE si le rendez-vous est un rendez-vous périodique et false si elle n’est pas périodique.
  
Cette propriété spécifie si l’objet représente ou non une série périodique. La valeur TRUE indique que l’objet représente une série périodique. La valeur FALSE, ou l’absence de cette propriété, indique que l’objet représente une instance unique ou une exception (y compris une instance orpheline). Notez la différence entre cette propriété et la propriété **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).
  
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

