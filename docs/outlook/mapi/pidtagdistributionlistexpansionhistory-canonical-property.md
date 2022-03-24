---
title: Propriété canonique PidTagDistributionListExpansionHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDistributionListExpansionHistory
api_type:
- HeaderDef
ms.assetid: fc1e0162-d655-4761-92e7-b469579c270b
description: Contient un historique montrant comment une liste de distribution a été étendue lors de la transmission du message.
ms.openlocfilehash: 13e5b2351a015b0db0bceef7e158cdd88e98a1ac
ms.sourcegitcommit: c68b7b7f98b3ff9e6de37ee5877adcad2e5e71d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63741982"
---
# <a name="pidtagdistributionlistexpansionhistory-canonical-property"></a>Propriété canonique PidTagDistributionListExpansionHistory

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un historique montrant comment une liste de distribution a été étendue lors de la transmission du message. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DL_EXPANSION_HISTORY  <br/> |
|Identificateur :  <br/> |0x0013  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est disponible pour les applications clientes de réception si le fournisseur de transport l’a définie. Il est également disponible pour le client d’envoi si le contenu du message est renvoyé avec un rapport. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagDistributionListExpansionProhibited](pidtagdistributionlistexpansionprohibited-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

