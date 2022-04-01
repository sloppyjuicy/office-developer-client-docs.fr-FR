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
description: Cette propriété contient un tableau binaire de méthodes de remise (fournisseurs de services), dans l’ordre des préférences de l’expéditeur d’un message.
ms.openlocfilehash: 2d8fc284b4c6f12069e512331424e477a337ea48
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523861"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>Propriété canonique PidTagRequestedDeliveryMethod

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient un tableau binaire de méthodes de remise (fournisseurs de services), dans l’ordre des préférences de l’expéditeur d’un message.
  
|Propriété |Valeur |
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

