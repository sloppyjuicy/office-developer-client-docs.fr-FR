---
title: Propriété canonique PidLidTaskStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383526"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>Propriété canonique PidLidTaskStartDate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Date lorsque l’utilisateur souhaite commencer la tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskStartDate  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x00008104  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Si la valeur de cette propriété est pas définie, la tâche n’a pas une date de début. La valeur « 0x5AE980E0 » (1,525,252,320) signifie également que la tâche n’a pas une date de début. Si la tâche a une date de début, la valeur doit avoir un composant de minuit et les **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) et les propriétés de **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) doivent également être définies.
  
Cette propriété est partagée par la spécification du protocole de signalisation d’information et spécification du protocole Task-Related objet situé dans [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les contacts et les listes de distribution personnelle.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propri�t� canonique PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
  
[Propri�t� canonique PidLidCommonStart](pidlidcommonstart-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

