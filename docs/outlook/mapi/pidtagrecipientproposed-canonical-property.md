---
title: Propriété canonique PidTagRecipientProposed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b09d8d7621121b3652ceb9824f6d36b53844206
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388055"
---
# <a name="pidtagrecipientproposed-canonical-property"></a>Propriété canonique PidTagRecipientProposed

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si un participant à la réunion a répondu.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_PROPOSED  <br/> |
|Identificateur :  <br/> |0x5FE1  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Destinataire de transport  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur TRUE pour cette propriété indique que le participant proposé une nouvelle date et/ou heure. La valeur FALSE, ou l’absence de cette propriété, signifie que le participant n’a pas encore répondu, soit la réponse la plus récente du participant ne pas inclure une nouvelle date / heure la proposition. Cette valeur ne doit pas avoir la valeur TRUE pour les participants d’une série périodique.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
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

