---
title: Propriété canonique PidLidTaskOrdinal
description: Décrit la propriété canonique PidLidTaskOrdinal, qui fournit une aide aux tâches de tri personnalisées. Cette propriété peut ne pas être spécifiée.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
ms.openlocfilehash: da90fa64ac22544fd540fb5e7db2e1a3ce00b4af
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817402"
---
# <a name="pidlidtaskordinal-canonical-property"></a>Propriété canonique PidLidTaskOrdinal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit une aide aux tâches de tri personnalisées.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskOrdinal  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x00008123  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut ne pas être spécifiée. Si elle est définie, sa valeur doit être supérieure à « 0x800186A0 » (-2 147 383 648) et inférieure à « 0x7FFE7960 » (2 147 383 648) et doit être unique parmi les tâches du même dossier.
  
Chaque fois que le client définit cette propriété sur un nombre inférieur au négatif de la valeur actuelle de la propriété **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) du dossier, le client doit également mettre à jour **PR_ORDINAL_MOST** sur le dossier. 
  
La **propriété PR_ORDINAL_MOST** du dossier fournit un moyen efficace de déterminer une valeur unique parmi les tâches du même dossier. 
  
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

