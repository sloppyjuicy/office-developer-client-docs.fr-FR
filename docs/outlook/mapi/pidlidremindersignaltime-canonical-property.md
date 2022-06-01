---
title: Propriété canonique PidLidReminderSignalTime
description: Décrit la propriété canonique PidLidReminderSignalTime, qui spécifie le point dans le temps où un rappel passe de l’attente au retard.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
ms.openlocfilehash: 36b52f3f9c9f02dc7a14e810bd8d558ef3388575
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817423"
---
# <a name="pidlidremindersignaltime-canonical-property"></a>Propriété canonique PidLidReminderSignalTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le point dans le temps où un rappel passe de l’attente au retard.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidReminderNextTime  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008560  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie si la propriété **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) a la valeur TRUE. Les clients doivent définir la valeur en temps universel coordonné (UTC).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour les rappels d’e-mail et d’autres objets.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

