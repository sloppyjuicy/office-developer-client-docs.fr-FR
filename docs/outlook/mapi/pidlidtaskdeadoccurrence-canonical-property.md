---
title: Propriété canonique PidLidTaskDeadOccurrence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0b740368aae43549e81cf3f4f6de40526c505b6b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401512"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a>Propriété canonique PidLidTaskDeadOccurrence

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si les nouvelles occurrences doivent être générés.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskDeadOccur  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x00008109  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Une périodicité n’est plus en vigueur lors de sa dernière instance est passée ou son nombre spécifié d’instances a été généré. Le client définit cette propriété sur FALSE pour une nouvelle tâche ou la valeur True lorsqu’il génère la dernière instance d’une tâche périodique. Lorsque vous copiez une tâche à générer une nouvelle instance, cette propriété est définie sur TRUE sur la copie, qui est l’instance terminée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche. 
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

