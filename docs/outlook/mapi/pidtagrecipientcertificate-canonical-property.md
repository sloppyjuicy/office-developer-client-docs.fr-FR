---
title: Propriété canonique PidTagRecipientCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bb51e9a602bd5c2e59bb56fdbf44fddc39651de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786532"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>Propriété canonique PidTagRecipientCertificate

  
  
**S’applique à**: Outlook 
  
Contient un certificat ASN.1 d’un destinataire de message pour une utilisation dans un rapport.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|Identificateur :  <br/> |0x0C13  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une copie de la propriété du destinataire **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) pour une utilisation dans un rapport. Il peut être utilisé pour prouver à l’expéditeur que le destinataire a effectivement reçu le message, un rapport de remise n’indique pas nécessairement.
  
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

