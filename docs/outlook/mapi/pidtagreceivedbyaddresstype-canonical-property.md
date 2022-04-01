---
title: Propriété canonique PidTagReceivedByAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: Contient le type d’adresse de messagerie, tel que SMTP, pour l’utilisateur de messagerie qui reçoit réellement le message.
ms.openlocfilehash: b5dfa7949ff0866fdecfb747b84d66d63d7d87ad
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64521865"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a>Propriété canonique PidTagReceivedByAddressType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le type d’adresse de messagerie, tel que SMTP, pour l’utilisateur de messagerie qui reçoit réellement le message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W  <br/> |
|Identificateur :  <br/> |0x0075  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse pour l’utilisateur de messagerie qui reçoit réellement le message. Elles doivent être définies par le fournisseur de transport entrant.
  
La chaîne de type d’adresse ne peut contenir que les caractères alphabétiques en minuscules A à Z et les nombres de zéro à neuf. Ces propriétés qualifient la propriété **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) en spécifiant un type d’adresse, tel que SMTP, indiquant ainsi comment l’adresse doit être construite.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les messages électroniques.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

