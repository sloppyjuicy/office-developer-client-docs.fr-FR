---
title: Propriété canonique PidLidTaskResetReminder
description: Décrit la propriété canonique PidLidTaskResetReminder, qui indique si les instances futures de tâches périodiques ont besoin de rappels.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
ms.openlocfilehash: 6fd9809a11664432416b882225dbb3a680835774
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816058"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a>Propriété canonique PidLidTaskResetReminder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si les futures instances de tâches périodiques ont besoin de rappels, même si **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) a la valeur FALSE.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskResetReminder  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008107  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Cette valeur est définie sur TRUE lorsque le rappel de la tâche est ignoré et défini sur FALSE dans le cas contraire. S’il n’est pas défini, la valeur par défaut false est supposée.
  
Comme spécifié dans [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), la propriété **dispidReminderSet** indique si un rappel est défini sur la tâche. Toutefois, cette propriété indique uniquement la présence d’un rappel sur une seule tâche. Elle ne peut pas être utilisée seule pour déterminer si une future instance d’une tâche périodique a besoin d’un rappel. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour des tâches.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour les rappels d’e-mail et d’autres objets.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propri�t� canonique PidLidReminderSet](pidlidreminderset-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

