---
title: Propriété canonique PidTagReplyRecipientNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355173"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a>Propriété canonique PidTagReplyRecipientNames

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste de noms d’affichage pour les destinataires devant obtenir une réponse.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W  <br/> |
|Identificateur :  <br/> |0x0050  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés contiennent les noms d’affichage séparés par des points-virgules.
  
Lorsque cette propriété n’est pas présente, une réponse est envoyée uniquement à l’utilisateur identifié par la **propriété PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)). Lorsque **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) et que ces propriétés sont définies, la réponse est envoyée à tous les destinataires identifiés par ces deux propriétés. Un fournisseur de transport utilise ces propriétés pour remplacer la logique de réponse habituelle.
  
Si **l PR_REPLY_RECIPIENT_ENTRIES** ou ces propriétés sont définies, l’autre propriété doit également être définie. Ces propriétés doivent contenir le même nombre de destinataires et elles doivent les contenir dans le même ordre. Le non-respect de ces exigences peut entraîner des résultats imprévisibles. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
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

