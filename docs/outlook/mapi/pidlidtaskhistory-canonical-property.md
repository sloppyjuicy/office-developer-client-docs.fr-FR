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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0e666e4ddcd72a50f3bcefdbfb2339d33d0123bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583687"
---
# <a name="pidlidtaskhistory-canonical-property"></a>Propriété canonique PidLidTaskHistory

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique le type de modification qui a été apporté pour la dernière fois à la tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskHistory  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x0000811A  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque la valeur de cette propriété est définie, la propriété **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) doit également être définie sur l’heure actuelle. Le tableau suivant indique les valeurs de la **propriété dispidTaskHistory,** répertoriées par ordre de priorité décroissante. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000004  <br/> |La **propriété dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) a été modifiée.  <br/> |
|0x00000003  <br/> |Une autre propriété a été modifiée.  <br/> |
|0x00000001  <br/> |L’affectation de la tâche a accepté cette tâche.  <br/> |
|0x00000002  <br/> |La personne à l’emploi de la tâche a rejeté cette tâche.  <br/> |
|0x00000005  <br/> |La tâche a été affectée à une personne affectée à la tâche.  <br/> |
|0x00000000  <br/> |Aucune modification n’a été apportée.  <br/> |
   
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

