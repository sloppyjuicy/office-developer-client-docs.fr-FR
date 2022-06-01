---
title: Propriété canonique PidLidReminderOverride
description: Décrit la propriété canonique PidLidReminderOverride, qui spécifie si le client doit respecter les valeurs des propriétés dispidReminderPlaySound.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidReminderOverride
api_type:
- COM
ms.assetid: ad7e37e1-bd12-409f-87e5-ebc0c298a072
ms.openlocfilehash: 6628a09d1b658782cddfdd1d13384a9fd06f3951
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817647"
---
# <a name="pidlidreminderoverride-canonical-property"></a>Propriété canonique PidLidReminderOverride

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si le client doit respecter les valeurs des propriétés **dispidReminderPlaySound** ([PidLidReminderPlaySound](pidlidreminderplaysound-canonical-property.md)) et **dispidReminderFileParam** ( [ PidLidReminderFileParameter](pidlidreminderfileparameter-canonical-property.md)).
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidReminderOverride  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x0000851C  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Remarques

Un client peut utiliser des valeurs par défaut à la place des valeurs des propriétés **dispidReminderPlaySound** et **dispidReminderFileParam** . 
  
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

