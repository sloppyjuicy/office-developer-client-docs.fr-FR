---
title: Propriété canonique PidLidTaskAssigners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385073"
---
# <a name="pidlidtaskassigners-canonical-property"></a>Propriété canonique PidLidTaskAssigners

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une pile d’entrées qui représentent des assigners de tâche. La plus récente assigne tâche s’affiche en haut de la pile.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskMyDelegators  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x00008117  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque le client reçoit une demande de tâche, il ajoute à cette propriété, la structure est définie dans [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), une entrée qui représente l’expéditeur de la tâche. Lorsque le client reçoit un refus de la tâche, le client supprime la dernière entrée assigne de tâche à partir de cette propriété. Lorsque le client envoie une réponse, il l’envoie à la dernière assigne tâche répertoriée dans la valeur de cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche 
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

