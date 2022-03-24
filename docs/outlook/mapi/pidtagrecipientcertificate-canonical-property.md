---
title: Propriété canonique PidTagRecipientCertificate
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a46e76f3fc23a8b50cea824387a024bed1964f19
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63716145"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>Propriété canonique PidTagRecipientCertificate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le certificat ASN.1 d’un destinataire de message à utiliser dans un état.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|Identificateur :  <br/> |0x0C13  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une copie de la propriété **PR_USER_CERTIFICATE (**[PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) du destinataire à utiliser dans un état. Elle peut être utilisée pour prouver à l’auteur que le destinataire a réellement reçu le message, ce qu’une note de remise n’indique pas nécessairement.
  
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

