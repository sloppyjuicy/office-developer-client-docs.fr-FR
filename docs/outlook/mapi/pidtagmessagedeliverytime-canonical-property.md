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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8ebaea7fb6888e51ee1ef658db53dcf3050644da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325612"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a>Propriété canonique PidTagMessageDeliveryTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date et l'heure auxquelles un message a été remis. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_DELIVERY_TIME  <br/> |
|Identificateur :  <br/> |0x0E06  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Heure du message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété décrit l'heure à laquelle le message a été stocké sur le serveur, et non le temps de téléchargement lorsque le fournisseur de transport a copié le message du serveur vers le magasin local.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

