---
title: Propriété canonique PidTagOriginalDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: Contient une copie de la date et de l’heure de remise du message d’origine dans un thread Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 49617214c6e797abdef3dd182cdf2c4fdccc28c7
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524561"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a>Propriété canonique PidTagOriginalDeliveryTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une copie de la date et de l’heure de remise du message d’origine dans un thread. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_DELIVERY_TIME  <br/> |
|Identificateur :  <br/> |0x0055  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est copiée à partir de la propriété **PR_MESSAGE_DELIVERY_TIME** d’origine ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans les opérations de réponse ou de forward suivantes et utilisée dans les rapports de lecture et non lus. Les rapports de remise **utilisent PR_DELIVER_TIME** propriété ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) à la place.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les objets de message électronique.
    
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

