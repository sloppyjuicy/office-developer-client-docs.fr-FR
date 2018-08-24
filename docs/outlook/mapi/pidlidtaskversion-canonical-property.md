---
title: Propriété canonique PidLidTaskVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 38bcf40f24cc7901ebcbb60a099dc0e797d8e4b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588033"
---
# <a name="pidlidtaskversion-canonical-property"></a>Propriété canonique PidLidTaskVersion

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Indique la copie est la dernière mise à jour d’une tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskVersion  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x00008112  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Mises à jour avec des versions inférieures à la tâche sont ignorés. 
  
Lors de l’incorporation d’une tâche dans une communication de la tâche, le client définit la version actuelle de la tâche incorporée sur ainsi que la communication de la tâche.
  
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

