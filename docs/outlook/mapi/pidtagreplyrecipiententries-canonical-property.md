---
title: Propriété canonique PidTagReplyRecipientEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: Contient un tableau de tailles d’identificateurs d’entrée pour les destinataires qui sont à obtenir une réponse. Cette propriété contient une structure et n’est pas une propriété à valeurs multiples.
ms.openlocfilehash: 5372fb32203d59c8c77cf3eb33a9d4c2a0ac5571
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63783041"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>Propriété canonique PidTagReplyRecipientEntries

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de tailles d’identificateurs d’entrée pour les destinataires qui sont à obtenir une réponse.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|Identificateur :  <br/> |0x004F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient une structure [FLATENTRYLIST](flatentrylist.md) et n’est pas une propriété à valeurs multiples. 
  
Lorsque cette propriété n’est pas présente, une réponse est envoyée uniquement à l’utilisateur identifié par la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). Lorsque les propriétés **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) sont définies, la réponse est envoyée à tous les destinataires identifiés par ces deux propriétés. Un fournisseur de transport utilise ces propriétés pour remplacer la logique de réponse habituelle.
  
Si cette propriété ou la **propriété PR_REPLY_RECIPIENT_NAMES** est définie, l’autre propriété doit également être définie. Ces propriétés doivent contenir le même nombre de destinataires et elles doivent les contenir dans le même ordre. Le non-respect de ces exigences peut entraîner des résultats imprévisibles. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les messages électroniques.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet en objets de message.
    
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

