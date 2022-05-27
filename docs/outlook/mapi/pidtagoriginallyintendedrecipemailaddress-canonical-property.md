---
title: Propriété canonique PidTagOriginallyIntendedRecipEmailAddress
description: Décrit la propriété canonique PidTagOriginallyIntendedRecipEmailAddress, qui contient l’adresse e-mail du destinataire prévu d’un message renvoyé automatiquement.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
ms.openlocfilehash: 8c5a6d1dd961ffc00e73ec2532977700897851b8
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752637"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a>Propriété canonique PidTagOriginallyIntendedRecipEmailAddress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’adresse e-mail du destinataire initialement prévu d’un message renvoyé automatiquement.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W  <br/> |
|Identificateur :  <br/> |0x007C  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse pour le destinataire du message initialement prévu. Ils doivent être définis par l’agent automatique qui a transféré le message.
  
Ces propriétés correspondent à l’attribut de rapport X.400 par destinataire.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

