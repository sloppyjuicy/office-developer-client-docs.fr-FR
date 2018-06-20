---
title: Propriété canonique PidLidTaskHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6e53d91a80d7e3b3bb4bf02ff3446eb385293c6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785474"
---
# <a name="pidlidtaskhistory-canonical-property"></a>Propriété canonique PidLidTaskHistory

  
  
**S’applique à**: Outlook 
  
Indique le type de modification qui a été effectué les dernières à la tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskHistory  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x0000811A  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque la valeur de cette propriété est définie, la propriété **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) doit également être définie à l’heure actuelle. Le tableau suivant indique les **dispidTaskHistory** valeurs de propriété, répertoriés par ordre décroissant de priorité. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 x 00000004  <br/> |Modifié de la propriété **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).  <br/> |
|0 x 00000003  <br/> |Une autre propriété a été modifiée.  <br/> |
|0x00000001  <br/> |Destinataire de la tâche acceptée cette tâche.  <br/> |
|0x00000002  <br/> |Destinataire de la tâche rejeté cette tâche.  <br/> |
|0 x 00000005  <br/> |La tâche a été affectée à un destinataire de la tâche.  <br/> |
|0x00000000  <br/> |Aucune modification n’a été apportée.  <br/> |
   
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

