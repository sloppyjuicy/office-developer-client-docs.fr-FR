---
title: Propriété canonique PidTagClientSubmitTime
description: Décrit la propriété canonique PidTagClientSubmitTime, qui contient la date et l’heure auxquelles l’expéditeur du message a envoyé un message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
ms.openlocfilehash: da635faaad0ca27d77f2188070c3322eb2381577
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817766"
---
# <a name="pidtagclientsubmittime-canonical-property"></a>Propriété canonique PidTagClientSubmitTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date et l’heure auxquelles l’expéditeur du message a envoyé un message. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CLIENT_SUBMIT_TIME  <br/> |
|Identificateur :  <br/> |0x0039  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Heure du message  <br/> |
   
## <a name="remarks"></a>Remarques

Le fournisseur de magasin définit **PR_CLIENT_SUBMIT_TIME** à l’heure à laquelle l’application cliente a appelé [IMessage::SubmitMessage](imessage-submitmessage.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

