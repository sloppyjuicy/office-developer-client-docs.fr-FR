---
title: Propriété canonique PidLidTaskDueDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e1712ede283dc4f1ec7996102f6033d647c18e8b
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455397"
---
# <a name="pidlidtaskduedate-canonical-property"></a>Propriété canonique PidLidTaskDueDate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente la date à laquelle l’utilisateur s’attend à effectuer la tâche.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskDueDate  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008105  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

La tâche n’a aucune date d’échéance si cette propriété n’est pas définie ou définie sur 0x5AE980E0 (1 525 252 320). Toutefois, une date d’échéance n’est facultative que si aucune date de début n’est indiquée dans la propriété **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)). Si la tâche a une date d’échéance, la valeur doit avoir un composant d’heure de minuit et la propriété **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) doit également être définie. Si **dispidTaskStartDate** a une date de début, la valeur de la propriété **dispidTaskDueDate** doit être supérieure ou égale à la valeur de **dispidTaskStartDate**.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.
    
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

