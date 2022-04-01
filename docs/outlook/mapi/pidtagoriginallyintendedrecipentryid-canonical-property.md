---
title: Propriété canonique PidTagOriginallyIntendedRecipEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: Contient l’identificateur d’entrée du destinataire initialement prévu d’un message transmis automatiquement. Cette propriété correspond à l’attribut d’état X.400 par destinataire.
ms.openlocfilehash: 6fc3849712e8f99bbf6b7f83bf8626ba86bb1708
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524160"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a>Propriété canonique PidTagOriginallyIntendedRecipEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée du destinataire initialement prévu d’un message transmis automatiquement.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINALLY_INTENDED_RECIP_ENTRYID  <br/> |
|Identificateur :  <br/> |0x1012  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est l’une des propriétés d’adresse du destinataire du message initialement prévu. Elle doit être définie par l’agent automatique qui a transmis le message.
  
Cette propriété correspond à l’attribut d’état X.400 par destinataire.
  
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

