---
title: PidLidTaskAssigner, propriété canonique
description: Décrit la propriété canonique, qui nomme l’utilisateur à qui la tâche a été attribuée pour la dernière fois et s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
ms.openlocfilehash: d57c4412d397df2b37fa732d016fa99724b39e0d
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818074"
---
# <a name="pidlidtaskassigner-canonical-property"></a>PidLidTaskAssigner, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Nomme l’utilisateur à qui la tâche a été attribuée pour la dernière fois. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskDelegator  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008121  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Si la tâche n’a pas été affectée, cette propriété n’est pas affectée. Étant donné que le client définit cette propriété une fois que l’assignateur de tâche reçoit une demande de tâche, la propriété ne sera pas définie sur la copie de la tâche par l’assignateur de tâches. Lorsque le client ajoute ou supprime un assigneur de tâches dans la liste des assigneurs de tâches dans la propriété **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), la propriété **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) doit être définie sur l’assigneur de tâche ajouté ou supprimé.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour des tâches.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

