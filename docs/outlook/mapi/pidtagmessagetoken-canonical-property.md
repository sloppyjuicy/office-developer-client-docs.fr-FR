---
title: Propriété canonique PidTagMessageToken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7357b7b98d90d08f7d14e965458703e4e193f63a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786246"
---
# <a name="pidtagmessagetoken-canonical-property"></a>Propriété canonique PidTagMessageToken

  
  
**S’applique à**: Outlook 
  
Contient un jeton de sécurité ASN.1 pour un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_TOKEN  <br/> |
|Identificateur :  <br/> |0x0C03  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Sécuriser les propriétés de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété véhicule protégées informations liées à la sécurité de son créateur à son destinataire. Conjointement avec la propriété **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), elle garantit association l’étiquette avec le contenu du message. Conjointement avec la propriété **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), il vérifie que le contenu du message est inchangé.
  
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

