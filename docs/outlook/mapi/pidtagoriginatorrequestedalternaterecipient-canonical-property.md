---
title: Propriété canonique PidTagOriginatorRequestedAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c7abd0ae93c5b38c756ec0915dda6a4cdfcebaa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786370"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a>Propriété canonique PidTagOriginatorRequestedAlternateRecipient

  
  
**S’applique à**: Outlook 
  
Contient un identificateur d’entrée pour un autre destinataire désigné par l’expéditeur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT  <br/> |
|Identificateur :  <br/> |0x0C09  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée dans les messages transféré automatiquement. Si le transfert automatique n’est pas autorisée ou si aucune autre destinataire n’a été désigné, un rapport de non-remise doit être généré.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

