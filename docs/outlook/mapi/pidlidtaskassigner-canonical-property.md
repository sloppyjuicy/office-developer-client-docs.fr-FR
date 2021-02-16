---
title: Propriété canonique PidLidTaskAssigner
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340088"
---
# <a name="pidlidtaskassigner-canonical-property"></a>Propriété canonique PidLidTaskAssigner

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Nomme l’utilisateur qui a été affecté pour la dernière fois à la tâche. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskDelegator  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008121  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Si la tâche n’a pas été affectée, cette propriété n’est pas affectée. Étant donné que le client définit cette propriété une fois que la personne à la tâche a reçu une demande de tâche, la propriété n’est pas définie sur la copie de la tâche de l’assigneur de la tâche. Lorsque le client ajoute ou supprime un assigneur de tâches de la liste des personnes qui affectent des tâches dans la propriété **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), la propriété **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) doit être définie sur l’assigneur de tâche ajouté ou supprimé.
  
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

