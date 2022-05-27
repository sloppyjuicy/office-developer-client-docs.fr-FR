---
title: Propriété canonique PidTagRecipientCertificate
description: Décrit la propriété canonique PidTagRecipientCertificate, qui contient le certificat ASN.1 d’un destinataire de message à utiliser dans un rapport.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
ms.openlocfilehash: 47f49c1fb4cfbb63b0c92611724fd9a6868d0a57
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752525"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>Propriété canonique PidTagRecipientCertificate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le certificat ASN.1 d’un destinataire de message à utiliser dans un rapport.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|Identificateur :  <br/> |0x0C13  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une copie de la propriété **PR_USER_CERTIFICATE** du destinataire ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) à utiliser dans un rapport. Il peut être utilisé pour prouver à l’expéditeur que le destinataire a effectivement reçu le message, ce qu’un rapport de remise n’indique pas nécessairement.
  
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

