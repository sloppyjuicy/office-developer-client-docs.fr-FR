---
title: Propriété canonique PidLidTaskAcceptanceState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 970fc57a3fd129f0ac50af3f71e0d5e15ff22371
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785436"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>Propriété canonique PidLidTaskAcceptanceState

  
  
**S’applique à**: Outlook 
  
Indique l’état d’acceptation de la tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskDelegValue  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x0000812A  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant présente les valeurs possibles pour cette propriété.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |La tâche n’est pas affectée.  <br/> |
|0x00000001  <br/> |Statut d’acceptation de la tâche est inconnue.  <br/> |
|0x00000002  <br/> |Destinataire de la tâche a accepté la tâche. Cette valeur est définie lorsque le client traite une acceptation de la tâche.  <br/> |
|0 x 00000003  <br/> |Destinataire de la tâche refusé la tâche. Cette valeur est définie lorsque le client traite un refus de tâche.  <br/> |
   
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

