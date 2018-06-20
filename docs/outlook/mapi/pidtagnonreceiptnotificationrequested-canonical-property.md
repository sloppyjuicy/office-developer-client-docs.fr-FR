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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 80c76242df409dbea1b60e423629b5b219e1d57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786267"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>Propriété canonique PidTagNonReceiptNotificationRequested

  
  
**S’applique à**: Outlook 
  
Contient la valeur TRUE si un expéditeur du message veut notification de non-réception pour un destinataire spécifié.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NON_RECEIPT_NOTIFICATION_REQUESTED  <br/> |
|Identificateur :  <br/> |0x0C06  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété contient la valeur FALSE et la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) contient la valeur TRUE, le fournisseur de services peut remplacer la propriété **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** et générer un rapport de non-remise. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

