---
title: Propriété canonique PidTagRequestedDeliveryMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8a2199ee2bba8b3b41af7bf26de6cdd3d8d0956e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786606"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>Propriété canonique PidTagRequestedDeliveryMethod

  
  
**S’applique à**: Outlook 
  
Cette propriété contient un tableau binaire de livraison (fournisseurs de services), par ordre de préférence de l’expéditeur d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REQUESTED_DELIVERY_METHOD  <br/> |
|Identificateur :  <br/> |0x0C18  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau contenu dans cette propriété se compose d’identificateurs ASN.1 pour chacun des fournisseurs de services.
  
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

