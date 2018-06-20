---
title: Propriété canonique PidTagReadReceiptEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 82bc5fd99df115527f703eff7261d02d1bf4d3ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786480"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a>Propriété canonique PidTagReadReceiptEntryId

  
  
**S’applique à**: Outlook 
  
Contient un identificateur d’entrée de l’utilisateur de messagerie où le système de messagerie doit diriger un rapport de lecture pour ce message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_READ_RECEIPT_ENTRYID  <br/> |
|Identificateur :  <br/> |0x0046  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est ignorée sauf si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie sur TRUE.
  
Si une application cliente doit recevoir une lu reports lui-même, il peut laisser cette propriété non définie ou définissez-la sur l’identificateur d’entrée contenue dans la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) au moment d’envoi de message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
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

