---
title: Propriété canonique PidTagMessageSubmissionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3a26a8483e584ccc5cf9f33e0dbd75f379c01633
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569665"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a>Propriété canonique PidTagMessageSubmissionId

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un identificateur de système (MTS) de transfert de message pour l’agent de transfert des messages (MTA).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_SUBMISSION_ID  <br/> |
|Identificateur :  <br/> |0x0047  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est retournée par le MTA en cas de réussite de l’envoi du message. N’importe quel contact futur avec le MTA concernant ce message, tel que demande l’annulation, utilise l’identificateur MTS dans cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

