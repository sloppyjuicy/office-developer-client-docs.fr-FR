---
title: Propriété canonique PidTagReplyRecipientEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1ab8828dd2fc28a2fba1620fc251ba0a87c3e2bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786576"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>Propriété canonique PidTagReplyRecipientEntries

  
  
**S’applique à**: Outlook 
  
Contient un tableau d’identificateurs d’entrée de taille pour les destinataires sont pour obtenir une réponse.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|Identificateur :  <br/> |0x004F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient une structure [FLATENTRYLIST](flatentrylist.md) et n’est pas une propriété à valeurs multiples. 
  
Lorsque cette propriété n’est pas présente, une réponse est envoyée uniquement à l’utilisateur identifié par la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). Lorsque ce et les propriétés **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) sont définies, la réponse est envoyée à tous les destinataires identifiés par ces deux propriétés. Un fournisseur de transport utilise ces propriétés pour remplacer la logique de réponse habituelle.
  
Si cette propriété ou la propriété **PR_REPLY_RECIPIENT_NAMES** est définie, l’autre propriété doit être définie également. Ces propriétés doivent contenir le même nombre de destinataires, et ils doivent contenir les dans le même ordre. Vous devez respecter ces conditions peut provoquer des résultats imprévisibles. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

