---
title: Propriété canonique PidLidReminderDelta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidReminderDelta
api_type:
- COM
ms.assetid: 011d73d0-8b38-4a4e-a56f-92dec451946a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f96317a5feb607637e3e8c6c689e8ba8ecaf8572
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630347"
---
# <a name="pidlidreminderdelta-canonical-property"></a>Propriété canonique PidLidReminderDelta

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’intervalle, en minutes, entre le moment où le rappel est en retard pour la première fois et l’heure de début de l’objet calendrier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidReminderDelta  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008501  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie sur les objets calendrier. Pour tous les objets non-calendrier, cette propriété doit être définie sur « 0x00000000 » et est ignorée. Lorsqu’un rappel est rejeté pour une instance d’un objet calendrier périodique, la valeur de cette propriété est utilisée dans le calcul de l’heure du signal pour l’instance suivante. Voir [[MS- OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) pour plus d’informations sur la création d’objets calendrier. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour les messages électroniques et autres rappels d’objets.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

