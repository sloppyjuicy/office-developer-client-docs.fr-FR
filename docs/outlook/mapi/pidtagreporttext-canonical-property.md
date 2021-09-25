---
title: Propriété canonique PidTagReportText
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 09bd3bdf-28d6-432c-9213-562a9a271adc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 94a951f06458cd24b50797e24d727b2f3bcaad8d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591548"
---
# <a name="pidtagreporttext-canonical-property"></a>Propriété canonique PidTagReportText

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient du texte facultatif pour un rapport généré par le système de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPORT_TEXT, PR_REPORT_TEXT_A, PR_REPORT_TEXT_W  <br/> |
|Identificateur :  <br/> |0x1001  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

En règle générale, le texte contenu dans ces propriétés est généré en réponse à un rapport de remise ou non remis, ou à un rapport de lecture ou non lu reçu du système de messagerie sous-jacent, mais n’est pas lui-même un texte transféré via ce système. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les messages électroniques.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

