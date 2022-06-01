---
title: Propriété canonique PidLidTaskAcceptanceState
description: Décrit la propriété canonique PidLidTaskAcceptanceState, qui indique l’état d’acceptation de la tâche.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
ms.openlocfilehash: eb210af71b8406032b28c3f8da61a704ac2f1a01
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817234"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>Propriété canonique PidLidTaskAcceptanceState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l’état d’acceptation de la tâche.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskDelegValue  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x0000812A  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant présente les valeurs possibles pour cette propriété.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |La tâche n’est pas affectée. |
|0x00000001  <br/> |L’état d’acceptation de la tâche est inconnu. |
|0x00000002  <br/> |L’assignateur de tâche a accepté la tâche. Cette valeur est définie lorsque le client traite une acceptation de tâche. |
|0x00000003  <br/> |L’assignateur de tâche a rejeté la tâche. Cette valeur est définie lorsque le client traite un rejet de tâche. |
   
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

