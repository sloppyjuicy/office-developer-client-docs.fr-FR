---
title: Propriété canonique PidTagReportText
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 09bd3bdf-28d6-432c-9213-562a9a271adc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8ef6117557b504678012b79e2b89c13bdaf6b787
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571485"
---
# <a name="pidtagreporttext-canonical-property"></a>Propriété canonique PidTagReportText

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le texte facultatif pour un rapport généré par le système de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPORT_TEXT, PR_REPORT_TEXT_A, PR_REPORT_TEXT_W  <br/> |
|Identificateur :  <br/> |0 x 1001  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

En règle générale, le texte contenu dans ces propriétés est généré en réponse à une remise ou rapport de non-remise ou un en lecture ou un état nonread reçu à partir du système de messagerie sous-jacent, mais n’est pas lui-même texte qui a été transféré par le biais de ce système. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

