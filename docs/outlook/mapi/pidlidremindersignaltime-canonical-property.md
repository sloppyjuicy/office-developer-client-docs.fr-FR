---
title: Propriété canonique PidLidReminderSignalTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3fcfd00f71a308dce625e6636edbe647f3d7258a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350854"
---
# <a name="pidlidremindersignaltime-canonical-property"></a>Propriété canonique PidLidReminderSignalTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique le moment où un rappel passe d'attente à en retard.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidReminderNextTime  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Common  <br/> |
|ID long (couvercle):  <br/> |0x00008560  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie si la propriété **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) a la valeur true. Les clients doivent définir la valeur au format UTC (Coordinated Universal Time).
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d'interaction pour les rappels de messagerie et d'objet.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

