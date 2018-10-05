---
title: Propriété canonique PidLidTaskFFixOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386263"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a>Propriété canonique PidLidTaskFFixOffline

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique la précision de la propriété **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskFFixOffline  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x0000812C  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Si la propriété **dispidTaskFFixOffline** est définie sur FALSE ou n’est pas définie, la valeur de la propriété **dispidTaskOwner** est correcte. Si **dispidTaskFFixOffline** est défini sur TRUE, le client ne peut pas déterminer une valeur précise de **dispidTaskOwner**. Dans ce cas, le client peut définir **dispidTaskOwner** à un nom de propriétaire générique, tel que « Inconnue ». Toutefois, si un client rencontre **dispidTaskFFixOffline** la valeur TRUE et peut déterminer un nom de propriétaire précis, le client doit mettre à jour **dispidTaskOwner** et **dispidTaskFFixOffline** la valeur FALSE. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche. 
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

