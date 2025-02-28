---
title: Propriété canonique PidLidTaskHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: Indique le type de modification qui a été apporté pour la dernière fois à la tâche. Lorsque cette propriété est définie, dispidTaskLastUpdate doit être définie sur l’heure actuelle.
ms.openlocfilehash: 8e9579b39ce2e0bf9102462b888ad2b6eb3bb8a3
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405726"
---
# <a name="pidlidtaskhistory-canonical-property"></a>Propriété canonique PidLidTaskHistory

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique le type de modification qui a été apporté pour la dernière fois à la tâche.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskHistory  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x0000811A  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque la valeur de cette propriété est définie, la propriété **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) doit également être définie sur l’heure actuelle. Le tableau suivant indique les valeurs **de propriété dispidTaskHistory** , répertoriées par ordre de priorité décroissante. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000004  <br/> |La **propriété dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) a été modifiée. |
|0x00000003  <br/> |Une autre propriété a été modifiée. |
|0x00000001  <br/> |L’affectation de la tâche a accepté cette tâche. |
|0x00000002  <br/> |L’affectation de la tâche a rejeté cette tâche. |
|0x00000005  <br/> |La tâche a été affectée à une personne affectée à la tâche. |
|0x00000000  <br/> |Aucune modification n’a été apportée. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

