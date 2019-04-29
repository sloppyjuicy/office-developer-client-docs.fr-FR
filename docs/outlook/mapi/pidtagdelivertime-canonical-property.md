---
title: Propriété canonique PidTagDeliverTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435277"
---
# <a name="pidtagdelivertime-canonical-property"></a>Propriété canonique PidTagDeliverTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date et l'heure auxquelles le message d'origine a été remis. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DELIVER_TIME  <br/> |
|Identificateur :  <br/> |0x0010  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une propriété par destinataire dans un rapport de remise qui indique l'heure à laquelle le message d'origine a été remis à l'utilisateur de messagerie pour lequel le rapport de remise est généré.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

