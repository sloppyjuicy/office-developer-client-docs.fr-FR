---
title: Propriété canonique PidTagNonReceiptNotificationRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419750"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>Propriété canonique PidTagNonReceiptNotificationRequested

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un expéditeur de message souhaite recevoir une notification de non-réception pour un destinataire spécifié.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NON_RECEIPT_NOTIFICATION_REQUESTED  <br/> |
|Identificateur :  <br/> |0x0C06  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété contient FALSE et que la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) contient TRUE, le fournisseur de services peut remplacer la propriété **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** et générer une non-remise. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

