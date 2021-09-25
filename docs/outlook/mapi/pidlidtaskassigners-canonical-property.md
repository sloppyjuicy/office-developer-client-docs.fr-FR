---
title: Propriété canonique PidLidTaskAssigners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1f72757c8a2104dd1f936d893fa226192981e740
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583708"
---
# <a name="pidlidtaskassigners-canonical-property"></a>Propriété canonique PidLidTaskAssigners

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une pile d’entrées qui représentent les personnes qui affectent des tâches. L’assigneur de tâches le plus récent apparaît en haut de la pile.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskMyDelegators  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008117  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque le client reçoit une demande de tâche, il l’append à cette propriété, dont la structure est définie dans [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), une entrée qui représente l’expéditeur de la tâche. Lorsque le client reçoit un rejet de tâche, il supprime la dernière entrée de l’assigneur de la tâche de cette propriété. Lorsque le client envoie une réponse de tâche, il l’envoie au dernier assigneur de tâche répertorié dans la valeur de cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches 
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

