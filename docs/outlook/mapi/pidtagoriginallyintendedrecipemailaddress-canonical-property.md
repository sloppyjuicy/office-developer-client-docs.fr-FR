---
title: Propriété canonique PidTagOriginallyIntendedRecipEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f4adbdfc041ebe5213c384db98343baa82af5b05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572724"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a>Propriété canonique PidTagOriginallyIntendedRecipEmailAddress

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient l’adresse de messagerie du destinataire prévu à l’origine d’un message transféré automatiquement.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W  <br/> |
|Identificateur :  <br/> |0x007C  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse pour le destinataire du message à l’origine. Il doivent être définies par l’agent automatique qui a transféré le message.
  
Ces propriétés correspondent à l’attribut par destinataire du rapport X.400.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

