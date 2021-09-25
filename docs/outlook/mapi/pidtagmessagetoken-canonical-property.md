---
title: Propriété canonique PidTagMessageToken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bfad9bbaea5f268bc85bb8fe58ff98ad24202470
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560843"
---
# <a name="pidtagmessagetoken-canonical-property"></a>Propriété canonique PidTagMessageToken

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un jeton de sécurité ASN.1 pour un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_TOKEN  <br/> |
|Identificateur :  <br/> |0x0C03  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés de messagerie sécurisée  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété transmet à son destinataire des informations de sécurité protégées de son auteur. Conjointement avec la **propriété PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), elle garantit l’association de l’étiquette avec le contenu du message. Conjointement avec la **propriété PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), il vérifie que le contenu du message est inchangé.
  
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

