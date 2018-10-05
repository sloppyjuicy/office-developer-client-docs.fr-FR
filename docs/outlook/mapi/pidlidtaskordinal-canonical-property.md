---
title: Propriété canonique PidLidTaskOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387733"
---
# <a name="pidlidtaskordinal-canonical-property"></a>Propriété canonique PidLidTaskOrdinal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit une aide pour des tâches de tri personnalisés.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskOrdinal  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x00008123  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut rester non définie. Si il est défini, sa valeur doit être supérieure à « 0x800186A0 » (-2,147,383,648) et inférieur à « 0x7FFE7960 » (2,147,383,648) et doit être unique parmi les tâches dans le même dossier.
  
Chaque fois que le client définit cette propriété sur une valeur inférieure à la valeur négative de la valeur actuelle de la propriété **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) du dossier, le client doit également mettre à jour **PR_ORDINAL_MOST** dans le dossier. 
  
La propriété **PR_ORDINAL_MOST** du dossier fournit un moyen efficace de déterminer une valeur unique entre les tâches dans le même dossier. 
  
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

