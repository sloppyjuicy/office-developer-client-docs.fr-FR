---
title: Propriété canonique PidTagRequestedDeliveryMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b7ba30b299d76f3a19464d5cba1a791ad115dc7e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570888"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>Propriété canonique PidTagRequestedDeliveryMethod

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient un tableau binaire de méthodes de remise (fournisseurs de services), dans l’ordre des préférences de l’expéditeur d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REQUESTED_DELIVERY_METHOD  <br/> |
|Identificateur :  <br/> |0x0C18  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau contenu dans cette propriété se compose d’identificateurs ASN.1 pour chacun des fournisseurs de services.
  
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

