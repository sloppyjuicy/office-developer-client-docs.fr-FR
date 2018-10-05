---
title: Propriété canonique PidTagMessageDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDeliveryTime
api_type:
- HeaderDef
ms.assetid: 4f9d44f2-4faa-4f16-9e33-22f80c17db85
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8ebaea7fb6888e51ee1ef658db53dcf3050644da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397344"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a>Propriété canonique PidTagMessageDeliveryTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date et l’heure quand un message a été remis. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_DELIVERY_TIME  <br/> |
|Identificateur :  <br/> |0x0E06  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Heure du message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété indique le moment où que le message a été stocké sur le serveur, plutôt que le temps de téléchargement lorsque le fournisseur de transport copié le message à partir du serveur dans le magasin local.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

