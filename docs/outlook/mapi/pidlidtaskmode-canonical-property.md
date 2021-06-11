---
title: Propriété canonique PidLidTaskMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357938"
---
# <a name="pidlidtaskmode-canonical-property"></a>Propriété canonique PidLidTaskMode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’état d’affectation de la tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskMode  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008518  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur doit être l’une des suivantes.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |La tâche n’est pas affectée.  <br/> |
|0x00000001  <br/> |La tâche est incorporée dans une demande de tâche.  <br/> |
|0x00000002  <br/> |La tâche a été acceptée par la personne à qui la tâche a été assignée.  <br/> |
|0x00000003  <br/> |La tâche a été rejetée par la personne assignée à la tâche.  <br/> |
|0x00000004  <br/> |La tâche est incorporée dans une mise à jour de tâche.  <br/> |
|0x00000005  <br/> |La tâche a été affectée à l’assigneur de la tâche.  <br/> |
   
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

