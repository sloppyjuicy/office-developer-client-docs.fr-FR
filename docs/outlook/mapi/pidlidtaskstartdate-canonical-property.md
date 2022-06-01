---
title: Propriété canonique PidLidTaskStartDate
description: Décrit la propriété canonique PidLidTaskStartDate, qui contient la date à laquelle l’utilisateur s’attend à commencer la tâche.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
ms.openlocfilehash: 568dd521b35d8280d0952e869bd9e2caf9d32d85
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816765"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>Propriété canonique PidLidTaskStartDate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Date à laquelle l’utilisateur s’attend à commencer la tâche.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskStartDate  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008104  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette valeur de propriété n’est pas spécifiée, la tâche n’a pas de date de début. La valeur « 0x5AE980E0 » (1 525 252 320) signifie également que la tâche n’a pas de date de début. Si la tâche a une date de début, la valeur doit avoir un composant d’heure de minuit, et les propriétés **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) et **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) doivent également être définies.
  
Cette propriété est partagée par la spécification du protocole d’indicateur d’information et Task-Related spécification du protocole objet située dans [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propri�t� canonique PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
  
[Propri�t� canonique PidLidCommonStart](pidlidcommonstart-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

