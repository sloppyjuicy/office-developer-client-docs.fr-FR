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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b4c497e77b9dfcea13742535148180275495717d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581866"
---
# <a name="pidlidtaskassigner-canonical-property"></a>Propriété canonique PidLidTaskAssigner

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 Noms de l’utilisateur qui a été affecté à la tâche. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskDelegator  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x00008121  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Si la tâche n’a pas été assignée, cette propriété est pas définie. Étant donné que le client définit cette propriété une fois que le destinataire de la tâche reçoit une demande de tâche, la propriété ne sera pas être définie sur la copie d’assigne la tâche de la tâche. Lorsque le client ajoute ou supprime un assigne des tâches de la liste des tâches assigne dans la propriété **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), la propriété **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) doit être définie sur l’ajout ou assigne une tâche supprimée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

