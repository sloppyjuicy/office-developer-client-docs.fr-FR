---
title: Propriété canonique PidLidTaskAssigners
description: Décrit la propriété canonique PidLidTaskAssigners, qui contient une pile d’entrées qui représentent les assignateurs de tâches.
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
ms.openlocfilehash: 8cb1dfc09774e5b83d14af8a3a031cff49ad2468
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816079"
---
# <a name="pidlidtaskassigners-canonical-property"></a>Propriété canonique PidLidTaskAssigners

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une pile d’entrées qui représentent les assignateurs de tâches. L’assignateur de tâche le plus récent apparaît en haut de la pile.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskMyDelegators  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008117  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque le client reçoit une demande de tâche, il ajoute à cette propriété, quelle structure est définie dans [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), une entrée qui représente l’expéditeur de la tâche. Lorsque le client reçoit un rejet de tâche, le client supprime la dernière entrée de l’assignateur de tâches de cette propriété. Lorsque le client envoie une réponse de tâche, le client l’envoie au dernier assigneur de tâche répertorié dans la valeur de cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour des tâches 
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

