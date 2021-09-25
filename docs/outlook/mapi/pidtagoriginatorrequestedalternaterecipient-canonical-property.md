---
title: Propriété canonique PidTagOriginatorRequestedAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f98a7cc97cae1fe548d079af0cad92b5f8e7a78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560773"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a>Propriété canonique PidTagOriginatorRequestedAlternateRecipient

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’entrée pour un autre destinataire désigné par l’expéditeur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT  <br/> |
|Identificateur :  <br/> |0x0C09  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée dans les messages autoforwarded. Si laforwarding automatique n’est pas autorisée ou si aucun autre destinataire n’a été désigné, un rapport de non-demande doit être généré.
  
## <a name="related-resources"></a>Ressources connexes

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

