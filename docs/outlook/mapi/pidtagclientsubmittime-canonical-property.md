---
title: Propriété canonique PidTagClientSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8c7ca5b2b6f5f3131c2fcb70ff0043825a68a91f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580123"
---
# <a name="pidtagclientsubmittime-canonical-property"></a>Propriété canonique PidTagClientSubmitTime

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la date et l’heure à laquelle que l’expéditeur du message envoyé un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CLIENT_SUBMIT_TIME  <br/> |
|Identificateur :  <br/> |0x0039  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Heure du message  <br/> |
   
## <a name="remarks"></a>Remarques

Le fournisseur de banque définit l’heure à laquelle l’application cliente appelée [IMessage::SubmitMessage](imessage-submitmessage.md) **PR_CLIENT_SUBMIT_TIME** . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
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

